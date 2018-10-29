---
UID: NF:d2d1_3helper.GradientMeshPatch
title: GradientMeshPatch function
author: windows-sdk-content
description: Creates a D2D1_GRADIENT_MESH_PATCH structure that contains the given control points, colors, and boundary flags.
old-location: direct2d\gradientmeshpatch.htm
tech.root: Direct2D
ms.assetid: 78d2af9d-e158-29ce-ea6e-67b2d22925a1
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GradientMeshPatch, GradientMeshPatch function [Direct2D], d2d1_3helper/GradientMeshPatch, direct2d.gradientmeshpatch
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - GradientMeshPatch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GradientMeshPatch function


## -description


Creates a <a href="https://msdn.microsoft.com/en-us/library/Dn890726(v=VS.85).aspx">D2D1_GRADIENT_MESH_PATCH</a> structure that contains the given control points, colors, and boundary flags.
        


## -parameters




### -param point00

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 00.


### -param point01

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 01.


### -param point02

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 02.


### -param point03

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 03.


### -param point10

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 10.


### -param point11

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 11.


### -param point12

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 12.


### -param point13

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 13.


### -param point20

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 20.


### -param point21

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 21.


### -param point22

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 22.


### -param point23

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 23.


### -param point30

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 30.


### -param point31

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 31.


### -param point32

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 32.


### -param point33

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a></b>

The coordinate-space location of the control point at position 33.


### -param color00

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368081(v=VS.85).aspx">D2D1_COLOR_F</a></b>

The color associated with the control point at position 00.


### -param color03

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368081(v=VS.85).aspx">D2D1_COLOR_F</a></b>

The color associated with the control point at position 03.


### -param color30

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368081(v=VS.85).aspx">D2D1_COLOR_F</a></b>

The color associated with the control point at position 30.


### -param color33

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368081(v=VS.85).aspx">D2D1_COLOR_F</a></b>

The color associated with the control point at position 33.


### -param topEdgeMode

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn986881(v=VS.85).aspx">D2D1_PATCH_EDGE_MODE</a></b>

Specifies how to render the top edge of the mesh.


### -param leftEdgeMode

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn986881(v=VS.85).aspx">D2D1_PATCH_EDGE_MODE</a></b>

Specifies how to render the left edge of the mesh.


### -param bottomEdgeMode

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn986881(v=VS.85).aspx">D2D1_PATCH_EDGE_MODE</a></b>

Specifies how to render the bottom edge of the mesh.


### -param rightEdgeMode

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn986881(v=VS.85).aspx">D2D1_PATCH_EDGE_MODE</a></b>

Specifies how to render the right edge of the mesh.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn890726(v=VS.85).aspx">D2D1_GRADIENT_MESH_PATCH</a></b>

Returns the created <a href="https://msdn.microsoft.com/en-us/library/Dn890726(v=VS.85).aspx">D2D1_GRADIENT_MESH_PATCH</a> structure.
          




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn890726(v=VS.85).aspx">D2D1_GRADIENT_MESH_PATCH</a>
 

 

