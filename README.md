>Notice: The repo fork from https://github.com/bricaud/gremlin-server-3.2.5-REST

# A Docker container for Gremlin 3.4 with a demo graph

This repository provides files to creates a container running a Gremlin server, [Gremlin Tinkerpop](https://github.com/apache/tinkerpop) 3.4.3, with a TinkerGraph. The graph database is populated with data from a tree of life (tree of 35960 nodes and 35959 edges, see data section). 
The licence is Apache 2.0 for the code files and Creative Commons BY 3 for the data.

## How to run it

To build it, run the following command:
```
./publish.sh test
```
  
  The Gremlin server will serve resquests on port 8182. 

On startup, the server loads the graph from the file `files/treeoflife.graphml`. 
See the [TinkerGraph configuration section](http://tinkerpop.apache.org/docs/current/reference/#_configuration_2) for more details.

Alternatively, you can pull the image from DockerHub [here](https://hub.docker.com/r/kineviz/gremlin-server/)
```
docker pull kineviz/gremlin-server
```

## Data
The data provided in the graphml file `files/treeoflife.graphml` is a tree of life.
The original data can be found on the [Tree Of Life Project website](http://tolweb.org/tree/home.pages/downloadtree.html) as a xml file (old xml version of the tree). Details about the data can be found on the same page.


The xml file available on the above website is licenced under the [Attribution Creative Commons 3.0](https://creativecommons.org/licenses/by/3.0/), the copyright is owned by the [Tree Of Life Project](http://tolweb.org/tree/home.pages/tolcopyright.html). It is available at `files/tolskeletaldumpUTF8.xml` (converted to UTF8).


The data has been extracted and saved as a graphml file to be easily loaded by the gremlin server.
The python script performing this task is provided as a Jupyter notebook `files/tree_of_life_xml_tol.ipynb` (APACHE 2.0 licence).
The content of the graphml file `files/treeoflife.graphml` is licenced under the same licence as the original xml file [Attribution Creative Commons 3.0](https://creativecommons.org/licenses/by/3.0/), the copyright is owned by Benjamin Ricaud. Copy, redistributions, modifications are allowed.
