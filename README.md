# Cube Auto UV - Automatically adjust UV coordinates for stretched cube meshes

Cube Auto UV is a script for the Godot Engine that automatically adjusts the UV coordinates of a cube mesh based on its parent's scale. This feature is particularly useful when working with cubes that are stretched or scaled unevenly, as it ensures that the texture applied to the cube does not become distorted but rather repeats seamlessly.

## How it Works

The script `cube_auto_uv.gd` extends the `Node` class in Godot Engine. It provides parameters to control which axes (x, y, z) should have their UV coordinates adjusted. By default, all axes are enabled for adjustment.

When the `_ready()` function is called, the script automatically adjusts the UV coordinates of the cube mesh according to the scale of its parent node. This ensures that the texture remains consistent even when the cube is stretched or scaled.

## Usage

1. Attach the `cube_auto_uv.gd` script to a node in your scene hierarchy.
2. Set the `parent` property to the `NodePath` of the parent node that contains the cube mesh.
3. Set the `mesh` property to the `NodePath` of the cube mesh node.
4. Optionally, you can control which axes (x, y, z) should have their UV coordinates adjusted by setting the corresponding boolean variables (`x_axis`, `y_axis`, `z_axis`).
5. Ensure that the material applied to the cube mesh has its UV1 scale set to `Vector3(3, 2, 1)` to match the adjusted UV coordinates.
6. Consider setting the size of the cube mesh to `Vector3(1, 1, 1)` if the default size of `Vector3(2, 2, 2)` does not fit your requirements.

## Example

An example usage of Cube Auto UV would be creating a long and high wall from a single cube by stretching it without needing to arrange many cubes manually.

Check out the `cube_example.tscn` file for an example of how to use the Snap to Grid Tool with a cube mesh.

## License

[![GNU AGPLv3 Image](https://www.gnu.org/graphics/agplv3-155x51.png)](https://www.gnu.org/licenses/agpl-3.0.html)

This program is Free Software: You can use, study share and improve it at your
will. Specifically you can redistribute and/or modify it under the terms of the
[GNU Affero General Public License](https://www.gnu.org/licenses/agpl-3.0.html) as
published by the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.
