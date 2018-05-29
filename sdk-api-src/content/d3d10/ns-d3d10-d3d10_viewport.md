---
UID: NS:d3d10.D3D10_VIEWPORT
title: D3D10_VIEWPORT
author: windows-sdk-content
description: Defines the dimensions of a viewport.
old-location: direct3d10\d3d10_viewport.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_viewport.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: D3D10_VIEWPORT, D3D10_VIEWPORT structure [Direct3D 10], d3d10/D3D10_VIEWPORT, direct3d10.d3d10_viewport, fabe1f82-a825-d3c2-8bfb-f2f706d1c57d
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d10.h
req.include-header: 
req.target-type: Windows
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
req.typenames: D3D10_VIEWPORT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D10.h
api_name:
-	D3D10_VIEWPORT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_VIEWPORT structure


## -description


Defines the dimensions of a <a href="https://msdn.microsoft.com/d78c3845-76fd-4bd7-a603-bb1d8c66ac49">viewport</a>.


## -struct-fields




### -field TopLeftX

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

X position of the left hand side of the viewport. Ranges between D3D10_VIEWPORT_BOUNDS_MIN and D3D10_VIEWPORT_BOUNDS_MAX.


### -field TopLeftY

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Y position of the top of the viewport. Ranges between D3D10_VIEWPORT_BOUNDS_MIN and D3D10_VIEWPORT_BOUNDS_MAX.


### -field Width

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Width of the viewport.


### -field Height

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Height of the viewport.


### -field MinDepth

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Minimum depth of the viewport. Ranges between 0 and 1.


### -field MaxDepth

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Maximum depth of the viewport. Ranges between 0 and 1.


## -remarks



In all cases, <b>Width</b> and <b>Height</b> must be ≥ 0 and <b>TopLeftX</b> + <b>Width</b> and <b>TopLeftY</b> + <b>Height</b> must be ≤ D3D10_VIEWPORT_BOUNDS_MAX.




## -see-also




<a href="https://msdn.microsoft.com/84769515-3f3b-4464-9620-7b806bf905b3">Core Structures</a>
 

 

