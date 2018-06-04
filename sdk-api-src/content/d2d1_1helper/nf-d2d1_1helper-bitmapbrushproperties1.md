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

# BitmapBrushProperties1 function


## -description


Creates a <a href="https://msdn.microsoft.com/0FECAD03-C35C-4729-9BBE-40DE11B34068">D2D1_BITMAP_BRUSH_PROPERTIES1</a> structure.


## -parameters




### -param extendModeX

TBD


### -param extendModeY

TBD


### -param interpolationMode

Type: <b><a href="direct2d.__D2D1_INTERPOLATION_MODE">D2D1_INTERPOLATION_MODE</a></b>

A value that specifies the interpolation algorithm that is used when images are scaled or rotated. The default value is <a href="direct2d.__D2D1_INTERPOLATION_MODE">D2D1_INTERPOLATION_MODE_LINEAR</a>.


#### - extendmodeX

Type: <b><a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE</a></b>

A value that specifies how the brush horizontally tiles those areas that extend past its bitmap. The default value is <a href="D2D1_EXTEND_MODE.htm">D2D1_EXTEND_MODE_CLAMP</a>. 


#### - extendmodeY

Type: <b><a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE</a></b>

A value that specifies how the brush vertically tiles those areas that extend past its bitmap. The default value is <a href="D2D1_EXTEND_MODE.htm">D2D1_EXTEND_MODE_CLAMP</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/0FECAD03-C35C-4729-9BBE-40DE11B34068">D2D1_BITMAP_BRUSH_PROPERTIES1</a></b>

A structure that describes the extend modes and the interpolation mode of an <a href="https://msdn.microsoft.com/5EF60CF5-DB7E-4453-80A2-F248A82A37E3">ID2D1BitmapBrush1</a>.



