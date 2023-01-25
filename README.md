# FireSat

[![Release](https://img.shields.io/github/v/tag/opencaesar/firesat-example?label=release)](https://github.com/opencaesar/firesat-example/releases/latest)

This is a description of a FireSat mission design expressed in OWL.

## Clone
```
  git clone https://github.com/melaasar/firesat.git
  cd firesat
```
## Prerequisites

- You need JDK 11+ installed in the environment

## Quick Start
Run the following
```
./gradlew startFuseki
./gradlew query
./gradlew stopFuseki
``` 
Inspect results of query in folder: `build/results` 

## Start Fuseki Server
Start a new Fuseki instance if one is not already started
```
./gradlew startFuseki
```
A Fuseki instance can now be accessed at URL: http://localhost:3030

> You need to run this once at the start before running any action (like load or query) involving Fuseki

## Stop Fuseki Server
Stop a running Fuseki instance if one is already running
```
./gradlew stopFuseki
```

> You need to run this once at the end after you are done running actions (like load or query) involving Fuseki

## Load Dataset
> Pre-req: A Fuseki server with a firesat dataset must be running at http://localhost:3030/firesat (see Start Fuseki Server below)  

Load a dataset to a running Fuseki instance
```
./gradlew load
```

## Query Dataset
>Pre-req: A Fuseki server with a firesat dataset must be running at http://localhost:3030/firesat (see Start Fuseki Server below)  

Run SPARQL queries in `src/sparql` on a dataset loaded in Fuseki
```
./gradlew query
```
Results will be in the folder `build/results`




