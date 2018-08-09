---
UID: NF:d2d1_3helper.GradientMeshPatchFromCoonsPatch
title: GradientMeshPatchFromCoonsPatch function
author: windows-sdk-content
description: Creates a D2D1_GRADIENT_MESH_PATCH from a given Coons patch description.
old-location: direct2d\gradientmeshpatchfromcoonspatch.htm
old-project: direct2d
ms.assetid: 12469ab9-890c-e4a9-57b2-41a804712052
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GradientMeshPatchFromCoonsPatch, GradientMeshPatchFromCoonsPatch function [Direct2D], d2d1_3helper/GradientMeshPatchFromCoonsPatch, direct2d.gradientmeshpatchfromcoonspatch
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d2d1_3helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - GradientMeshPatchFromCoonsPatch
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# GradientMeshPatchFromCoonsPatch function


## -description


Creates a <a href="https://msdn.microsoft.com/16d1ef03-f0c9-7414-d54d-9513199272aa">D2D1_GRADIENT_MESH_PATCH</a> from a given Coons patch description.
        


## -parameters




### -param point0

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 0.


### -param point1

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 1.


### -param point2

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 2.


### -param point3

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 3.


### -param point4

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 4.


### -param point5

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 5.


### -param point6

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 6.


### -param point7

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 7.


### -param point8

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 8.


### -param point9

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 9.


### -param point10

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 10.


### -param point11

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 11.


### -param color0

Type: <b><a href="https://msdn.microsoft.com/564d4f41-2da7-49ed-b85a-d1070d662b40">D2D1_COLOR_F</a></b>

The color associated with the control point at position 0.


### -param color1

Type: <b><a href="https://msdn.microsoft.com/564d4f41-2da7-49ed-b85a-d1070d662b40">D2D1_COLOR_F</a></b>

The color associated with the control point at position 1.


### -param color2

Type: <b><a href="https://msdn.microsoft.com/564d4f41-2da7-49ed-b85a-d1070d662b40">D2D1_COLOR_F</a></b>

The color associated with the control point at position 2.


### -param color3

Type: <b><a href="https://msdn.microsoft.com/564d4f41-2da7-49ed-b85a-d1070d662b40">D2D1_COLOR_F</a></b>

The color associated with the control point at position 3.


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
          




## -remarks



The following image shows the numbering of control points in a Coons patch.

<img alt="Numbering of control points in a Coons patch" src="images/coonspatch.png"/>



## -see-also




<a href="https://msdn.microsoft.com/16d1ef03-f0c9-7414-d54d-9513199272aa">D2D1_GRADIENT_MESH_PATCH</a>
 

 

