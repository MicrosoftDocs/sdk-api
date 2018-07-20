---
UID: NS:d2d1_1.D2D1_BITMAP_BRUSH_PROPERTIES1
title: D2D1_BITMAP_BRUSH_PROPERTIES1
author: windows-sdk-content
description: Describes the extend modes and the interpolation mode of an ID2D1BitmapBrush.
old-location: direct2d\d2d1_bitmap_brush_properties1.htm
old-project: direct2d
ms.assetid: 0FECAD03-C35C-4729-9BBE-40DE11B34068
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: D2D1_BITMAP_BRUSH_PROPERTIES1, D2D1_BITMAP_BRUSH_PROPERTIES1 structure [Direct2D], d2d1_1/D2D1_BITMAP_BRUSH_PROPERTIES1, direct2d.d2d1_bitmap_brush_properties1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d2d1_1.h
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
req.typenames: D2D1_BITMAP_BRUSH_PROPERTIES1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1_1.h
api_name:
 - D2D1_BITMAP_BRUSH_PROPERTIES1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D2D1_BITMAP_BRUSH_PROPERTIES1 structure


## -description



    Describes the extend modes and the interpolation mode of an <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a>.


## -struct-fields




### -field extendModeX

Type: <b><a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE</a></b>

A value that describes how the brush horizontally tiles those areas that extend past its bitmap.


### -field extendModeY

Type: <b><a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE</a></b>

A value that describes how the brush vertically tiles those areas that extend past its bitmap.


### -field interpolationMode

Type: <b><a href="https://msdn.microsoft.com/library/Hh447004(v=VS.85).aspx">D2D1_INTERPOLATION_MODE</a></b>

A value that specifies how the bitmap is interpolated when it is scaled or rotated.


## -see-also




<a href="https://msdn.microsoft.com/b53b7e0a-aa8b-4788-896c-9825c9e6cceb">D2D1_BITMAP_INTERPOLATION_MODE</a>



<a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE</a>
 

 

