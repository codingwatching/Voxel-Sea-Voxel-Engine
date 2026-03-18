# Voxel Sea — Voxel Engine

A custom voxel engine built to explore terrain generation, chunk-based world systems, and performance tradeoffs in Roblox.

## DEMO Game:

The Voxaria - Build Anything! codebase: https://github.com/OptimizedFunction/Voxaria
The Voxaria - Build Anything! Roblox game: https://www.roblox.com/games/6699108984/

## Overview

Voxel Sea is a personal project focused on building a scalable voxel world system from the ground up. The engine explores how voxel data is structured, generated, and updated efficiently in real time, within Roblox’s constraints.

## Features

- Chunk-based world system for scalable terrain
- Procedural terrain generation
- Dynamic voxel updates
- Parallel Luau usage to accelerate terrain generation
- Greedy meshing using Parts for voxel surface generation

## Architecture

The engine is structured around a chunked world model:

- The world is divided into chunks, each containing a grid of voxels  
- Chunks are generated and updated independently  
- Terrain generation is parallelized using Parallel Luau to improve performance  
- Greedy meshing is used to reduce part count by merging adjacent voxel faces  

Due to the lack of editable mesh support at the time, terrain is represented using Parts rather than custom mesh geometry.

## Focus Areas

This project focuses on understanding and implementing core voxel engine concepts:

- Efficient chunk management and updates  
- Parallelizing terrain generation  
- Reducing part count through greedy meshing  
- Working within engine constraints to achieve acceptable performance  

## Why this is interesting

Voxel engines require careful handling of data locality, generation cost, and rendering constraints. On Roblox, these challenges are amplified due to limitations around mesh generation and part counts.

This project explores how to build a performant voxel system within those constraints, including leveraging Parallel Luau for generation and using greedy meshing to make large voxel worlds feasible.

## Notes

This is a technical exploration project aimed at understanding voxel system architecture and performance tradeoffs, rather than a full production-ready engine.
