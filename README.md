gravizo
=======

How to include graphviz graphs in github README.md

###New. The indirect way.###
You can use indirect way to refer a source file as graph description. 
Use this sintax: ```![Alt text](https://g.gravizo.com/source/<custom_mark>?<url_source_url_encoded>```). And use html div tag ```<div> </div>``` (some graphs uses --> so don't use html comments) to hide the source followed by your description graph in [DOT syntax](https://en.wikipedia.org/wiki/DOT_(graph_description_language)), [UMLGraph](http://www.umlgraph.org/doc/cd-intro.html), [PlantUML](http://plantuml.sourceforge.net/sequence.html) or [SVG](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics) :

![Alt text](https://g.gravizo.com/source/custom_mark10?https%3A%2F%2Fraw.githubusercontent.com%2FTLmaK0%2Fgravizo%2Ffix%2FREADME%2FREADME.md)
<div style="display:none">
custom_mark10
  digraph G {
    aize ="4,4";
    main [shape=box];
    main -> parse [weight=8];
    parse -> execute;
    main -> init [style=dotted];
    main -> cleanup;
    execute -> { make_string; printf};
    init -> make_string;
    edge [color=red];
    main -> printf [style=bold,label="100 times"];
    make_string [label="make a string"];
    node [shape=box,style=filled,color=".7 .3 1.0"];
    execute -> compare;
  }
custom_mark10
</div>

```
![Alt text](https://g.gravizo.com/source/custom_mark10?https%3A%2F%2Fraw.githubusercontent.com%2FTLmaK0%2Fgravizo%2Ffix%2FREADME%2FREADME.md)
<div>
custom_mark10
  digraph G {
    aize ="4,4";
    main [shape=box];
    main -> parse [weight=8];
    parse -> execute;
    main -> init [style=dotted];
    main -> cleanup;
    execute -> { make_string; printf};
    init -> make_string;
    edge [color=red];
    main -> printf [style=bold,label="100 times"];
    make_string [label="make a string"];
    node [shape=box,style=filled,color=".7 .3 1.0"];
    execute -> compare;
  }
custom_mark10
</div>
```

This allows to include your graphs in the README, and still redeable in normal text editor.

**SVG output** it's ready. Only need to replace https://g.gravizo.com/g? by https://g.gravizo.com/svg? and https://g.gravizo.com/source? by https://g.gravizo.com/source/svg?

![Alt text](https://g.gravizo.com/source/custom_mark11?https%3A%2F%2Fraw.githubusercontent.com%2FTLmaK0%2Fgravizo%2Ffix%2FREADME%2FREADME.md)
<div>
custom_mark11
  digraph G {
    aize ="4,4";
    main [shape=box];
    main -> parse [weight=8];
    parse -> execute;
    main -> init [style=dotted];
    main -> cleanup;
    execute -> { make_string; printf};
    init -> make_string;
    edge [color=red];
    main -> printf [style=bold,label="100 times"];
    make_string [label="make a string"];
    node [shape=box,style=filled,color=".7 .3 1.0"];
    execute -> compare;
  }
custom_mark11
</div>

```
![Alt text](https://g.gravizo.com/source/custom_mark11?https%3A%2F%2Fraw.githubusercontent.com%2FTLmaK0%2Fgravizo%2Ffix%2FREADME%2FREADME.md)
<div>
custom_mark11
  digraph G {
    aize ="4,4";
    main [shape=box];
    main -> parse [weight=8];
    parse -> execute;
    main -> init [style=dotted];
    main -> cleanup;
    execute -> { make_string; printf};
    init -> make_string;
    edge [color=red];
    main -> printf [style=bold,label="100 times"];
    make_string [label="make a string"];
    node [shape=box,style=filled,color=".7 .3 1.0"];
    execute -> compare;
  }
custom_mark11
</div>
```

![Alt text](https://g.gravizo.com/source/custom_mark12?https%3A%2F%2Fraw.githubusercontent.com%2FTLmaK0%2Fgravizo%2Ffix%2FREADME%2FREADME.md)
<div>
custom_mark12
/** 
*Structural Things
*@opt commentname
*@note Notes can
*be extended to
*span multiple lines
*/
class Structural{}
/**
*@opt all
*@note Class
*/
class Counter extends Structural {
        static public int counter;
        public int getCounter%28%29;
}
/**
*@opt shape activeclass
*@opt all
*@note Active Class
*/
class RunningCounter extends Counter{}
)
custom_mark12
</div>
```
![Alt text](https://g.gravizo.com/source/custom_mark12?https%3A%2F%2Fraw.githubusercontent.com%2FTLmaK0%2Fgravizo%2Ffix%2FREADME%2FREADME.md)
<div>
custom_mark12
/** 
*Structural Things
*@opt commentname
*@note Notes can
*be extended to
*span multiple lines
*/
class Structural{}
/**
*@opt all
*@note Class
*/
class Counter extends Structural {
        static public int counter;
        public int getCounter%28%29;
}
/**
*@opt shape activeclass
*@opt all
*@note Active Class
*/
class RunningCounter extends Counter{}
)
custom_mark12
</div>
```

A sequence diagram. Note that you need to include ; in each new line:

![Alt text](https://g.gravizo.com/source/custom_mark13?https%3A%2F%2Fraw.githubusercontent.com%2FTLmaK0%2Fgravizo%2Ffix%2FREADME%2FREADME.md)
<div>
custom_mark13
@startuml;
actor User;
participant "First Class" as A;
participant "Second Class" as B;
participant "Last Class" as C;
User -> A: DoWork;
activate A;
A -> B: Create Request;
activate B;
B -> C: DoWork;
activate C;
C -> B: WorkDone;
destroy C;
B -> A: Request Created;
deactivate B;
A -> User: Done;
deactivate A;
@enduml
custom_mark13
</div>

```
![Alt text](https://g.gravizo.com/source/custom_mark13?https%3A%2F%2Fraw.githubusercontent.com%2FTLmaK0%2Fgravizo%2Ffix%2FREADME%2FREADME.md)
<div>
custom_mark13
@startuml;
actor User;
participant "First Class" as A;
participant "Second Class" as B;
participant "Last Class" as C;
User -> A: DoWork;
activate A;
A -> B: Create Request;
activate B;
B -> C: DoWork;
activate C;
C -> B: WorkDone;
destroy C;
B -> A: Request Created;
deactivate B;
A -> User: Done;
deactivate A;
@enduml
custom_mark13
</div>
```

An activity diagram. Note that you need to include ; in each new line:

![Alt text](https://g.gravizo.com/source/custom_activity?https%3A%2F%2Fraw.githubusercontent.com%2FTLmaK0%2Fgravizo%2Ffix%2FREADME%2FREADME.md)
<div>
custom_activity
@startuml;
%28*%29 --> if "Some Test" then;
  -->[true] "activity 1";
  if "" then;
    -> "activity 3" as a3;
  else;
    if "Other test" then;
      -left-> "activity 5";
    else;
      --> "activity 6";
    endif;
  endif;
else;
  ->[false] "activity 2";
endif;
a3 --> if "last test" then;
  --> "activity 7";
else;
  -> "activity 8";
endif;
@enduml
custom_activity
</div>

```
![Alt text](https://g.gravizo.com/source/custom_activity?https%3A%2F%2Fraw.githubusercontent.com%2FTLmaK0%2Fgravizo%2Ffix%2FREADME%2FREADME.md)
<div>
custom_activity
@startuml;
%28*%29 --> if "Some Test" then;
  -->[true] "activity 1";
  if "" then;
    -> "activity 3" as a3;
  else;
    if "Other test" then;
      -left-> "activity 5";
    else;
      --> "activity 6";
    endif;
  endif;
else;
  ->[false] "activity 2";
endif;
a3 --> if "last test" then;
  --> "activity 7";
else;
  -> "activity 8";
endif;
@enduml
custom_activity
</div>
```

Now also suports SVG in JSON format:

![Alt text](https://g.gravizo.com/source/custom_svg?https%3A%2F%2Fraw.githubusercontent.com%2FTLmaK0%2Fgravizo%2Ffix%2FREADME%2FREADME.md)
<div>
custom_svg
@gravizosvg
{"svg": {
		"@height": "450",
		"@width": "450", 
		"path": [
			{"@id":"lineAB", "@d": "M 100 350 l 150 -300", "@stroke":"red"},
			{"@id":"lineBC", "@d": "M 250 50 l 150 300", "@stroke":"red"},
			{"@d":"M 100 350 q 150 -300 300 0", "@stroke":"blue", "@fill":"none"}
    ],
		"g": [
			{"@stroke":"black", "circle":[  
				{"@id":"pointA", "@cx":"100", "@cy":"350", "@r":"3"},
				{"@id":"pointB", "@cx":"250", "@cy":"50", "@r":"3"},
				{"@id":"pointC", "@cx":"400", "@cy":"350", "@r":"3"}
			]},
			{"text": [
				{"@x":"100", "@y":"350", "@dx":"-30", "$":"A"},
				{"@x":"250", "@y":"50", "@dy":"-10", "$":"B"},
				{"@x":"400", "@y":"350", "@dx":"30", "$":"C"}
			]}
		]
	}
}
)
custom_svg
</div>

```
![Alt text](https://g.gravizo.com/source/custom_svg?https%3A%2F%2Fraw.githubusercontent.com%2FTLmaK0%2Fgravizo%2Ffix%2FREADME%2FREADME.md)
<div>
custom_svg
@gravizosvg
{"svg": {
		"@height": "450",
		"@width": "450", 
		"path": [
			{"@id":"lineAB", "@d": "M 100 350 l 150 -300", "@stroke":"red"},
			{"@id":"lineBC", "@d": "M 250 50 l 150 300", "@stroke":"red"},
			{"@d":"M 100 350 q 150 -300 300 0", "@stroke":"blue", "@fill":"none"}
    ],
		"g": [
			{"@stroke":"black", "circle":[  
				{"@id":"pointA", "@cx":"100", "@cy":"350", "@r":"3"},
				{"@id":"pointB", "@cx":"250", "@cy":"50", "@r":"3"},
				{"@id":"pointC", "@cx":"400", "@cy":"350", "@r":"3"}
			]},
			{"text": [
				{"@x":"100", "@y":"350", "@dx":"-30", "$":"A"},
				{"@x":"250", "@y":"50", "@dy":"-10", "$":"B"},
				{"@x":"400", "@y":"350", "@dx":"30", "$":"C"}
			]}
		]
	}
}
)
custom_svg
</div>
```
