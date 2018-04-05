---
UID: NE:d3d9types.D3DSCANLINEORDERING
title: D3DSCANLINEORDERING
author: windows-driver-content
description: Flags indicating the method the rasterizer uses to create an image on a surface.
old-location: direct3d9\D3DSCANLINEORDERING.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dscanlineordering.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 5851669a-6c7f-d88e-d11f-c33b6cce7b2c, D3DSCANLINEORDERING, D3DSCANLINEORDERING enumeration [Direct3D 9], D3DSCANLINEORDERING_INTERLACED, D3DSCANLINEORDERING_PROGRESSIVE, LPD3DSCANLINEORDERING, LPD3DSCANLINEORDERING enumeration pointer [Direct3D 9], d3d9types/D3DSCANLINEORDERING, d3d9types/D3DSCANLINEORDERING_INTERLACED, d3d9types/D3DSCANLINEORDERING_PROGRESSIVE, d3d9types/LPD3DSCANLINEORDERING, direct3d9.D3DSCANLINEORDERING
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3d9types.h
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
req.typenames: D3DSCANLINEORDERING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DSCANLINEORDERING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3DSCANLINEORDERING enumeration


## -description


Flags indicating the method the rasterizer uses to create an image on a surface.


## -enum-fields




### -field D3DSCANLINEORDERING_UNKNOWN


### -field D3DSCANLINEORDERING_PROGRESSIVE

The image is created from the first scanline to the last without skipping any.


### -field D3DSCANLINEORDERING_INTERLACED

The image is created using the interlaced method in which odd-numbered lines are drawn on odd-numbered passes and even lines are drawn on even-numbered passes.


## -remarks



This enumeration is used as a member in <a href="https://msdn.microsoft.com/4a03d0f0-dec5-4209-8c99-b58cc13064f5">D3DDISPLAYMODEFILTER</a> and <a href="https://msdn.microsoft.com/df9d12b9-7acb-435b-9d54-0b095c871f0e">D3DDISPLAYMODEEX</a>.




## -see-also




<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

