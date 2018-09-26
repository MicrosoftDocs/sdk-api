---
UID: NE:d2d1effectauthor.D2D1_VERTEX_OPTIONS
title: D2D1_VERTEX_OPTIONS
author: windows-sdk-content
description: Describes flags that influence how the renderer interacts with a custom vertex shader.
old-location: direct2d\d2d1_vertex_options.htm
tech.root: direct2d
ms.assetid: b308aaf4-edf0-49a8-8fbf-04bb38c00605
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: D2D1_VERTEX_OPTIONS, D2D1_VERTEX_OPTIONS enumeration [Direct2D], D2D1_VERTEX_OPTIONS_ASSUME_NO_OVERLAP, D2D1_VERTEX_OPTIONS_DO_NOT_CLEAR, D2D1_VERTEX_OPTIONS_NONE, D2D1_VERTEX_OPTIONS_USE_DEPTH_BUFFER, d2d1effectauthor/D2D1_VERTEX_OPTIONS, d2d1effectauthor/D2D1_VERTEX_OPTIONS_ASSUME_NO_OVERLAP, d2d1effectauthor/D2D1_VERTEX_OPTIONS_DO_NOT_CLEAR, d2d1effectauthor/D2D1_VERTEX_OPTIONS_NONE, d2d1effectauthor/D2D1_VERTEX_OPTIONS_USE_DEPTH_BUFFER, direct2d.d2d1_vertex_options
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: D2d1.lib; D2d1.dll
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2d1.lib
 - D2d1.dll
api_name:
 - D2D1_VERTEX_OPTIONS
product: Windows
targetos: Windows
req.typenames: D2D1_VERTEX_OPTIONS
req.redist: 
---

# D2D1_VERTEX_OPTIONS enumeration


## -description


Describes flags that influence how the renderer interacts with a custom vertex shader.


## -enum-fields




### -field D2D1_VERTEX_OPTIONS_NONE

The logical equivalent of having no flags set.


### -field D2D1_VERTEX_OPTIONS_DO_NOT_CLEAR

If this flag is set, the renderer  assumes that the vertex shader will cover the entire region of interest with vertices and need not clear the destination render target. If this flag is not set, the renderer assumes that the vertices do not cover the entire region interest and must clear the render target to transparent black first.


### -field D2D1_VERTEX_OPTIONS_USE_DEPTH_BUFFER

The renderer will use a depth buffer when rendering custom vertices. The depth buffer will be used for calculating occlusion information. This can result in the renderer output being draw-order dependent if it contains transparency.


### -field D2D1_VERTEX_OPTIONS_ASSUME_NO_OVERLAP

Indicates that custom vertices do not overlap each other.


### -field D2D1_VERTEX_OPTIONS_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/5f4c7248-9303-4451-92f1-4b230efd627a">D2D1_BLEND_DESCRIPTION</a>



<a href="https://msdn.microsoft.com/0DC46758-6005-4A33-9539-9C95CF8CFB6A">ID2D1BlendTransform</a>
 

 

