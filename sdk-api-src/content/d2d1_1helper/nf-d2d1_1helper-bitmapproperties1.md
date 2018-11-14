---
UID: NF:d2d1_1helper.BitmapProperties1
title: BitmapProperties1 function
author: windows-sdk-content
description: Creates a D2D1_BITMAP_PROPERTIES1 structure.
old-location: direct2d\bitmapproperties1.htm
tech.root: direct2d
ms.assetid: 68391380-4C53-41EA-8458-EFD4387396D3
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: BitmapProperties1, BitmapProperties1 function [Direct2D], d2d1_1helper/BitmapProperties1, direct2d.bitmapproperties1
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
 - BitmapProperties1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- BitmapProperties1
: 
---

# BitmapProperties1 function


## -description


Creates a <a href="https://msdn.microsoft.com/en-us/library/Hh404275(v=VS.85).aspx">D2D1_BITMAP_PROPERTIES1</a> structure.


## -parameters




### -param bitmapOptions

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh446984(v=VS.85).aspx">D2D1_BITMAP_OPTIONS</a></b>

A combination of <a href="https://msdn.microsoft.com/en-us/library/Hh446984(v=VS.85).aspx">D2D1_BITMAP_OPTIONS</a>-typed values that specify how the bitmap can be used.


### -param pixelFormat [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Dd368138(v=VS.85).aspx">D2D1_PIXEL_FORMAT</a></b>

The bitmap's pixel format and alpha mode. The default value is a <a href="https://msdn.microsoft.com/en-us/library/Dd368138(v=VS.85).aspx">D2D1_PIXEL_FORMAT</a> with a <b>format</b> of <a href="http://msdn.microsoft.com/en-us/library/bb173059(VS.85).aspx">DXGI_FORMAT_UNKNOWN</a> and an <b>alphaMode</b> of  <a href="https://msdn.microsoft.com/en-us/library/Dd368058(v=VS.85).aspx">D2D1_ALPHA_MODE_UNKNOWN</a>. For more information about pixel formats, see <a href="https://msdn.microsoft.com/en-us/library/Dd756766(v=VS.85).aspx">Supported Pixel Formats and Alpha Modes</a>.


### -param dpiX

Type: <b>FLOAT</b>

The horizontal dpi of the bitmap. The default value is 96.0f. 


### -param dpiY

Type: <b>FLOAT</b>

The vertical dpi of the bitmap. The default value is 96.0f.


### -param colorContext [in]

Type: <b><a href="https://msdn.microsoft.com/acdda11e-eb3f-4258-b24e-daa3b7a23fd6">ID2D1ColorContext</a>*</b>

An optional pointer to the <a href="https://msdn.microsoft.com/acdda11e-eb3f-4258-b24e-daa3b7a23fd6">ID2D1ColorContext</a> interface for a color context to use with the bitmap. If you don't want to specify a color context, set this parameter to <b>NULL</b>. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh404275(v=VS.85).aspx">D2D1_BITMAP_PROPERTIES1</a></b>

A <a href="https://msdn.microsoft.com/en-us/library/Hh404275(v=VS.85).aspx">D2D1_BITMAP_PROPERTIES1</a> structure that describes the bitmap.



