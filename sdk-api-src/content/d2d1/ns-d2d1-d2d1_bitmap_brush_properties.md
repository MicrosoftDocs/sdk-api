---
UID: NS:d2d1.D2D1_BITMAP_BRUSH_PROPERTIES
title: D2D1_BITMAP_BRUSH_PROPERTIES
author: windows-sdk-content
description: Describes the extend modes and the interpolation mode of an ID2D1BitmapBrush.
old-location: direct2d\D2D1_BITMAP_BRUSH_PROPERTIES.htm
tech.root: Direct2D
ms.assetid: e252d1b4-2f34-4479-94fc-636d4115b00c
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: D2D1_BITMAP_BRUSH_PROPERTIES, D2D1_BITMAP_BRUSH_PROPERTIES structure [Direct2D], d2d1/D2D1_BITMAP_BRUSH_PROPERTIES, direct2d.D2D1_BITMAP_BRUSH_PROPERTIES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d2d1.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_BITMAP_BRUSH_PROPERTIES
product: Windows
targetos: Windows
req.typenames: D2D1_BITMAP_BRUSH_PROPERTIES
req.redist: 
---

# D2D1_BITMAP_BRUSH_PROPERTIES structure


## -description


Describes the extend modes and the interpolation mode of an <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a>.


## -struct-fields




### -field extendModeX

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368100(v=VS.85).aspx">D2D1_EXTEND_MODE</a></b>

A value that describes how the brush horizontally tiles those areas that extend past its bitmap.


### -field extendModeY

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368100(v=VS.85).aspx">D2D1_EXTEND_MODE</a></b>

A value that describes how the brush vertically tiles those areas that extend past its bitmap.


### -field interpolationMode

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368073(v=VS.85).aspx">D2D1_BITMAP_INTERPOLATION_MODE</a></b>

A value that specifies how the bitmap is interpolated when it is scaled or rotated.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd368073(v=VS.85).aspx">D2D1_BITMAP_INTERPOLATION_MODE</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd368100(v=VS.85).aspx">D2D1_EXTEND_MODE</a>
 

 

