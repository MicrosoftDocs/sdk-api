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
 

 

