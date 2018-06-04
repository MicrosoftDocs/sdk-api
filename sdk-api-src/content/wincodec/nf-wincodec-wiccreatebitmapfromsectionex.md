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

# WICCreateBitmapFromSectionEx function


## -description


Returns a <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a> that is backed by the pixels of a Windows Graphics Device Interface (GDI) section handle.


## -parameters




### -param width [in]

Type: <b>UINT</b>

The width of the bitmap pixels.


### -param height [in]

Type: <b>UINT</b>

The height of the bitmap pixels.


### -param pixelFormat

Type: <b><a href="_wic_codec_native_pixel_formats.htm">REFWICPixelFormatGUID</a></b>

The pixel format of the bitmap.


### -param hSection [in]

Type: <b>HANDLE</b>

The section handle. This is a file mapping object handle returned by the <a href="https://msdn.microsoft.com/d3302183-76a0-47ec-874f-1173db353dfe">CreateFileMapping</a> function.


### -param stride [in]

Type: <b>UINT</b>

The byte count of each scanline.


### -param offset [in]

Type: <b>UINT</b>

The offset into the section.


### -param desiredAccessLevel [in]

Type: <b><a href="https://msdn.microsoft.com/4b08bc8c-d67c-4bc4-a701-2903a971a478">WICSectionAccessLevel</a></b>

The desired access level.


### -param ppIBitmap

TBD




#### - pIBitmap [out]

Type: <b><a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a>**</b>

A pointer that receives the bitmap.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



