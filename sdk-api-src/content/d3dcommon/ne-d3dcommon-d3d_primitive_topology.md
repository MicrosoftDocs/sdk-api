---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# D3D_PRIMITIVE_TOPOLOGY enumeration


## -description


Values that indicate how the pipeline interprets vertex data that is bound to the <a href="https://msdn.microsoft.com/71141a5e-2d79-4b02-8370-c0cbc8618908">input-assembler stage</a>. These <a href="https://msdn.microsoft.com/357ad085-fd91-4420-abc3-1c57e8cbb517">primitive topology values</a> determine how the vertex data is rendered on screen.


## -enum-fields




### -field D3D_PRIMITIVE_TOPOLOGY_UNDEFINED

The IA stage has not been initialized with a primitive topology. The IA stage will not function properly unless a primitive topology is defined.


### -field D3D_PRIMITIVE_TOPOLOGY_POINTLIST

Interpret the vertex data as a list of points.


### -field D3D_PRIMITIVE_TOPOLOGY_LINELIST

Interpret the vertex data as a list of lines.


### -field D3D_PRIMITIVE_TOPOLOGY_LINESTRIP

Interpret the vertex data as a line strip.


### -field D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST

Interpret the vertex data as a list of triangles.


### -field D3D_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP

Interpret the vertex data as a triangle strip.


### -field D3D_PRIMITIVE_TOPOLOGY_LINELIST_ADJ

Interpret the vertex data as a list of lines with adjacency data.


### -field D3D_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ

Interpret the vertex data as a line strip with adjacency data.


### -field D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ

Interpret the vertex data as a list of triangles with adjacency data.


### -field D3D_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ

Interpret the vertex data as a triangle strip with adjacency data.


### -field D3D_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D10_PRIMITIVE_TOPOLOGY_UNDEFINED

The IA stage has not been initialized with a primitive topology. The IA stage will not function properly unless a primitive topology is defined.


### -field D3D10_PRIMITIVE_TOPOLOGY_POINTLIST

Interpret the vertex data as a list of points.


### -field D3D10_PRIMITIVE_TOPOLOGY_LINELIST

Interpret the vertex data as a list of lines.


### -field D3D10_PRIMITIVE_TOPOLOGY_LINESTRIP

Interpret the vertex data as a line strip.


### -field D3D10_PRIMITIVE_TOPOLOGY_TRIANGLELIST

Interpret the vertex data as a list of triangles.


### -field D3D10_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP

Interpret the vertex data as a triangle strip.


### -field D3D10_PRIMITIVE_TOPOLOGY_LINELIST_ADJ

Interpret the vertex data as a list of lines with adjacency data.


### -field D3D10_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ

Interpret the vertex data as a line strip with adjacency data.


### -field D3D10_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ

Interpret the vertex data as a list of triangles with adjacency data.


### -field D3D10_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ

Interpret the vertex data as a triangle strip with adjacency data.


### -field D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED

The IA stage has not been initialized with a primitive topology. The IA stage will not function properly unless a primitive topology is defined.


### -field D3D11_PRIMITIVE_TOPOLOGY_POINTLIST

Interpret the vertex data as a list of points.


### -field D3D11_PRIMITIVE_TOPOLOGY_LINELIST

Interpret the vertex data as a list of lines.


### -field D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP

Interpret the vertex data as a line strip.


### -field D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST

Interpret the vertex data as a list of triangles.


### -field D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP

Interpret the vertex data as a triangle strip.


### -field D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ

Interpret the vertex data as a list of lines with adjacency data.


### -field D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ

Interpret the vertex data as a line strip with adjacency data.


### -field D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ

Interpret the vertex data as a list of triangles with adjacency data.


### -field D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ

Interpret the vertex data as a triangle strip with adjacency data.


### -field D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


### -field D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST

Interpret the vertex data as a patch list.


## -remarks



Use the  <a href="https://msdn.microsoft.com/a9896b34-b273-4be2-bea4-0fcecdf5bcad">ID3D11DeviceContext::IASetPrimitiveTopology</a> method and a value from <b>D3D_PRIMITIVE_TOPOLOGY</b> to bind a primitive topology to the input-assembler stage. Use the  <a href="https://msdn.microsoft.com/99f82993-72c2-47b5-a2fe-16bb1e7bd2e3">ID3D11DeviceContext::IAGetPrimitiveTopology</a> method to retrieve the primitive topology for the input-assembler stage.

The following diagram shows the various primitive types for a geometry shader object.

<img alt="Illustration of the various primitive types for a geometry shader object" border="" src="images/D3D11_GSInputs1.png"/>



## -see-also




<a href="https://msdn.microsoft.com/002154d5-74a6-48fb-b55f-8687e4505fc7">Common Version Enumerations</a>
 

 

