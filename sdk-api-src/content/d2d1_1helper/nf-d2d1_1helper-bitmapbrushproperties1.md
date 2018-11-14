---
UID: NF:d2d1_1helper.BitmapBrushProperties1
title: BitmapBrushProperties1 function
author: windows-sdk-content
description: Creates a D2D1_BITMAP_BRUSH_PROPERTIES1 structure.
old-location: direct2d\bitmapbrushproperties1.htm
tech.root: direct2d
ms.assetid: 83F8641B-9BE4-4BBD-99FD-215EA3BD371A
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: BitmapBrushProperties1, BitmapBrushProperties1 function [Direct2D], d2d1_1helper/BitmapBrushProperties1, direct2d.bitmapbrushproperties1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1_1helper.h
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
 - BitmapBrushProperties1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- BitmapBrushProperties1
: 
---

# BitmapBrushProperties1 function


## -description


Creates a <a href="https://msdn.microsoft.com/0FECAD03-C35C-4729-9BBE-40DE11B34068">D2D1_BITMAP_BRUSH_PROPERTIES1</a> structure.


## -parameters




### -param extendModeX

Type: <b><a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE</a></b>

A value that specifies how the brush horizontally tiles those areas that extend past its bitmap. The default value is <a href="D2D1_EXTEND_MODE.htm">D2D1_EXTEND_MODE_CLAMP</a>. 


### -param extendModeY

Type: <b><a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE</a></b>

A value that specifies how the brush vertically tiles those areas that extend past its bitmap. The default value is <a href="D2D1_EXTEND_MODE.htm">D2D1_EXTEND_MODE_CLAMP</a>.


### -param interpolationMode

Type: <b><a href="direct2d.__D2D1_INTERPOLATION_MODE">D2D1_INTERPOLATION_MODE</a></b>

A value that specifies the interpolation algorithm that is used when images are scaled or rotated. The default value is <a href="direct2d.__D2D1_INTERPOLATION_MODE">D2D1_INTERPOLATION_MODE_LINEAR</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/0FECAD03-C35C-4729-9BBE-40DE11B34068">D2D1_BITMAP_BRUSH_PROPERTIES1</a></b>

A structure that describes the extend modes and the interpolation mode of an <a href="https://msdn.microsoft.com/5EF60CF5-DB7E-4453-80A2-F248A82A37E3">ID2D1BitmapBrush1</a>.



