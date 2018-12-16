---
UID: NF:d2d1helper.BitmapProperties
title: BitmapProperties function
author: windows-sdk-content
description: Creates a D2D1_BITMAP_PROPERTIES structure.
old-location: direct2d\bitmapproperties.htm
tech.root: direct2d
ms.assetid: 5f85602a-3706-4cd6-8124-07e06be2d29c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BitmapProperties, BitmapProperties function [Direct2D], d2d1helper/BitmapProperties, direct2d.bitmapproperties
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
 - BitmapProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BitmapProperties function


## -description


Creates a <a href="https://msdn.microsoft.com/050246fd-f91a-4a2a-858a-5f0447e3ecbf">D2D1_BITMAP_PROPERTIES</a> structure.


## -parameters




### -param pixelFormat [ref]

Type: <b>const <a href="https://msdn.microsoft.com/e95afd9c-5793-4cb7-bcb8-aae4d28b6532">D2D1_PIXEL_FORMAT</a></b>

The bitmap's pixel format and alpha mode. The default value is a <a href="https://msdn.microsoft.com/e95afd9c-5793-4cb7-bcb8-aae4d28b6532">D2D1_PIXEL_FORMAT</a> with a <b>format</b> of <a href="http://msdn.microsoft.com/en-us/library/bb173059(VS.85).aspx">DXGI_FORMAT_UNKNOWN</a> and an <b>alphaMode</b> of  <a href="https://msdn.microsoft.com/f1b1e735-2e89-4dc1-9fee-dfb4626ef453">D2D1_ALPHA_MODE_UNKNOWN</a>. For more information about pixel formats, see <a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel Formats and Alpha Modes</a>.


### -param dpiX

Type: <b>FLOAT</b>

The horizontal dpi of the bitmap. The default value is 96.0f. 


### -param dpiY

Type: <b>FLOAT</b>

The vertical dpi of the bitmap. The default value is 96.0f.


## -returns



Type: <b><a href="https://msdn.microsoft.com/050246fd-f91a-4a2a-858a-5f0447e3ecbf">D2D1_BITMAP_PROPERTIES</a></b>

A structure that describes the pixel format and dpi 
    of a bitmap. 




## -see-also




<a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>
 

 

