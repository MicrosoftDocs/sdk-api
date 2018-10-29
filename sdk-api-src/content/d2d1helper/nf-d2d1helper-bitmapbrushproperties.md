---
UID: NF:d2d1helper.BitmapBrushProperties
title: BitmapBrushProperties function
author: windows-sdk-content
description: Creates a D2D1_BITMAP_BRUSH_PROPERTIES structure.
old-location: direct2d\bitmapbrushproperties.htm
tech.root: Direct2D
ms.assetid: 8945b4d8-0d6e-4f23-9a0b-1ec690339bdd
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: BitmapBrushProperties, BitmapBrushProperties function [Direct2D], d2d1helper/BitmapBrushProperties, direct2d.bitmapbrushproperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1helper.h
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
 - BitmapBrushProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BitmapBrushProperties function


## -description


Creates a <a href="https://msdn.microsoft.com/e252d1b4-2f34-4479-94fc-636d4115b00c">D2D1_BITMAP_BRUSH_PROPERTIES</a> structure.


## -parameters




### -param extendModeX

Type: <b><a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE</a></b>

A value that specifies how the brush horizontally tiles those areas that extend past its bitmap. The default value is <a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE CLAMP</a>. 


### -param extendModeY

Type: <b><a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE</a></b>

A value that specifies how the brush vertically tiles those areas that extend past its bitmap. The default value is <a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE CLAMP</a>.


### -param interpolationMode

Type: <b><a href="https://msdn.microsoft.com/b53b7e0a-aa8b-4788-896c-9825c9e6cceb">D2D1_BITMAP_INTERPOLATION_MODE</a></b>

A value that specifies the interpolation algorithm that is used when images are scaled or rotated. The default value is <a href="https://msdn.microsoft.com/b53b7e0a-aa8b-4788-896c-9825c9e6cceb">D2D1_BITMAP_INTERPOLATION_MODE_LINEAR</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/e252d1b4-2f34-4479-94fc-636d4115b00c">D2D1_BITMAP_BRUSH_PROPERTIES</a></b>

A structure that describes the extend modes and the interpolation mode of an <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a>.




## -see-also




<a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a>
 

 

