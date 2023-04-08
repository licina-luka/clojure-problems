# clojure-problems
Knowledgebase of common problems

## Unknown tool: tools

Commonly presents as an error during an attempt to add Sean Cornfield's "new" like so

```
clojure -Ttools install io.github.seancorfield/deps-new '{:git/tag "v0.5.1"}' :as new
```

and the error 

```Error building classpath. Unknown tool: tools```

### Solution

(https://clojurians-log.clojureverse.org/clj-on-windows/2022-09-01) is to create `~/.clojure/tools/tools.edn` and add in

```
{:lib io.github.clojure/tools.tools
 :coord {:git/tag "v0.2.8"
         :git/sha "9c5baa56cff02de98737a71d4dab098b268cd68b"}}

```
or newer before re-running 
