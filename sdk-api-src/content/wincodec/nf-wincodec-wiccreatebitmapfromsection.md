---
UID: NF:wincodec.WICCreateBitmapFromSection
title: WICCreateBitmapFromSection function
author: windows-driver-content
description: Returns a IWICBitmapSource that is backed by the pixels of a Windows Graphics Device Interface (GDI) section handle.
old-location: wic\_wic_codec_wiccreatebitmapfromsection.htm
old-project: wic
ms.assetid: a14022a0-7af6-4c06-9afa-4709b81efc96
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: WICCreateBitmapFromSection, WICCreateBitmapFromSection function [Windows Imaging Component], _wic_codec_wiccreatebitmapfromsection, wic._wic_codec_wiccreatebitmapfromsection, wincodec/WICCreateBitmapFromSection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Windowscodecs.dll
-	Wincodec.lib
api_name:
-	WICCreateBitmapFromSection
product: Windows
targetos: Windows
req.lib: 
req.dll: Windowscodecs.dll; Wincodec.lib
req.irql: 
req.product: Windows Address Book 5.0
---

# WICCreateBitmapFromSection function


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


### -param ppIBitmap

TBD




#### - pIBitmap [out]

Type: <b><a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a>**</b>

A pointer that receives the bitmap.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>WICCreateBitmapFromSection</b> function calls the <a href="https://msdn.microsoft.com/0c9892a5-c136-41f6-8161-8077afe1a9da">WICCreateBitmapFromSectionEx</a> function with the <i>desiredAccessLevel</i> parameter set to <b>WICSectionAccessLevelRead</b>.



