Pack of plugins to move your LIT assets from Unity to Marmoset 4/5




Unity Setup





Place the MiniJson file into the Assets folder.



Place the export script into the Assets/Editor folder.



Place the SlotDictionary.txt file in the same folder as the export script.



Enable the FBX Exporter package via the Unity Package Manager.



Launch the plugin via Tools → MaterialDataExportTool. This tool provides two checkboxes (to export textures and to export material data as JSON) and a button to trigger the standard FBX Exporter.



Marmoset Setup





In Marmoset Toolbag, go to Edit → Plugins → Show User Plugin Folder.



Place the AssignTexturesFromJSON.py import script into this folder.



Overall Workflow





Export the JSON, textures, and FBX from Unity using the MaterialDataExportTool.



Import the exported FBX file into Marmoset Toolbag.



In Marmoset, go to Edit → Plugins → AssignTexturesFromJSON to run the import script.



Voilà — your textures are automatically assigned.




Video instruction: 
https://youtu.be/2IXPbueTjiU


P.S. If any of your textures are not listed in the JSON, try modifying the SlotDictionary.txt file. This file tells the script how to match texture slots from the Unity shader to the texture slots in the Marmoset shader. For example, the standard Unity Lit shader uses _BumpMap for the Normal Map, but this can be different in custom shaders or other Unity rendering pipelines.

My advice would be to open the material shader file in a text viewer to identify the texture slot names, and then match them accordingly in the SlotDictionary.txt file.
