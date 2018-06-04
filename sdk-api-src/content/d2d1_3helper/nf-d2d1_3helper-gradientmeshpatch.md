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

# GradientMeshPatch function


## -description



          Creates a <a href="https://msdn.microsoft.com/16d1ef03-f0c9-7414-d54d-9513199272aa">D2D1_GRADIENT_MESH_PATCH</a> structure that contains the given control points, colors, and boundary flags.
        


## -parameters




### -param point00

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 00.


### -param point01

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 01.


### -param point02

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 02.


### -param point03

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 03.


### -param point10

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 10.


### -param point11

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 11.


### -param point12

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 12.


### -param point13

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 13.


### -param point20

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 20.


### -param point21

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 21.


### -param point22

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 22.


### -param point23

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 23.


### -param point30

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 30.


### -param point31

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 31.


### -param point32

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 32.


### -param point33

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 33.


### -param color00

Type: <b><a href="https://msdn.microsoft.com/564d4f41-2da7-49ed-b85a-d1070d662b40">D2D1_COLOR_F</a></b>

The color associated with the control point at position 00.


### -param color03

Type: <b><a href="https://msdn.microsoft.com/564d4f41-2da7-49ed-b85a-d1070d662b40">D2D1_COLOR_F</a></b>

The color associated with the control point at position 03.


### -param color30

Type: <b><a href="https://msdn.microsoft.com/564d4f41-2da7-49ed-b85a-d1070d662b40">D2D1_COLOR_F</a></b>

The color associated with the control point at position 30.


### -param color33

Type: <b><a href="https://msdn.microsoft.com/564d4f41-2da7-49ed-b85a-d1070d662b40">D2D1_COLOR_F</a></b>

The color associated with the control point at position 33.


### -param topEdgeMode

Type: <b><a href="https://msdn.microsoft.com/5AE38632-B068-4A14-9DAB-67FD58E3894B">D2D1_PATCH_EDGE_MODE</a></b>

Specifies how to render the top edge of the mesh.


### -param leftEdgeMode

Type: <b><a href="https://msdn.microsoft.com/5AE38632-B068-4A14-9DAB-67FD58E3894B">D2D1_PATCH_EDGE_MODE</a></b>

Specifies how to render the left edge of the mesh.


### -param bottomEdgeMode

Type: <b><a href="https://msdn.microsoft.com/5AE38632-B068-4A14-9DAB-67FD58E3894B">D2D1_PATCH_EDGE_MODE</a></b>

Specifies how to render the bottom edge of the mesh.


### -param rightEdgeMode

Type: <b><a href="https://msdn.microsoft.com/5AE38632-B068-4A14-9DAB-67FD58E3894B">D2D1_PATCH_EDGE_MODE</a></b>

Specifies how to render the right edge of the mesh.


## -returns



Type: <b><a href="https://msdn.microsoft.com/16d1ef03-f0c9-7414-d54d-9513199272aa">D2D1_GRADIENT_MESH_PATCH</a></b>


            Returns the created <a href="https://msdn.microsoft.com/16d1ef03-f0c9-7414-d54d-9513199272aa">D2D1_GRADIENT_MESH_PATCH</a> structure.
          




## -see-also




<a href="https://msdn.microsoft.com/16d1ef03-f0c9-7414-d54d-9513199272aa">D2D1_GRADIENT_MESH_PATCH</a>
 

 

