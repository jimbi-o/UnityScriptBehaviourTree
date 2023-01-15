# UnityScriptBehaviourTree
Unity custom package for scripting behaviour tree.

## What Is This Package?

* A set of scripts to build behaviour tree for Unity.
  * Behaviour tree is well described [here](https://www.gamedeveloper.com/programming/behavior-trees-for-ai-how-they-work).
* Provides a set of basic behaviour tree nodes.
  * composite
    * `sequence`
    * `selection`
  * decorator
    * `repeat`
    * `repeat_until_fail`
    * `inverter`
    * `succeeder`
* Accepts a set of delegates from user for each tasks.
* Uses JSON to express graph structure.
  * It does not provide GUI to build trees.
  * [Online JSON to Tree Diagram Converter](https://vanya.jp.net/vtree/) and [Editor | JSON Crack](https://jsoncrack.com/editor) are great to visualize JSON graphs.
* Provides a simple blackboard.

## Getting Started

1. In your project's Packages/manifest.json, add `"com.jimbio.behaviourtree": "https://github.com/jimbi-o/UnityScriptBehaviourTree.git"` to `dependencies`.
1. Open Window > Package Manager.
1. Click + button on left top.
1. Select "Add package from git URL..."
1. type `com.jimbio.behaviourtree`
1. Click Install.

## How to Use

1. Write a JSON file to express graph structure ([Sample](Samples~/BehaviourTree/Params/BT.json)).
1. Provide sets of methods for each tasks (leaf nodes of the behaviour tree).
1. Create an instance of BehaviourTreeSet.
1. Call Tick method to update behaviour tree.

* Check [BTTest.cs](Samples~/BehaviourTree/Scripts/BTTest.cs) for sample code.
* Import sample from Package Manager to see it working.
