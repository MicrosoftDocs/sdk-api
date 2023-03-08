---
UID: NF:wincodec.WICCreateBitmapFromSection
title: WICCreateBitmapFromSection function (wincodec.h)
description: Returns a IWICBitmapSource that is backed by the pixels of a Windows Graphics Device Interface (GDI) section handle. (WICCreateBitmapFromSection)
helpviewer_keywords: ["WICCreateBitmapFromSection","WICCreateBitmapFromSection function [Windows Imaging Component]","_wic_codec_wiccreatebitmapfromsection","wic._wic_codec_wiccreatebitmapfromsection","wincodec/WICCreateBitmapFromSection"]
old-location: wic\_wic_codec_wiccreatebitmapfromsection.htm
tech.root: wic
ms.assetid: a14022a0-7af6-4c06-9afa-4709b81efc96
ms.date: 12/05/2018
ms.keywords: WICCreateBitmapFromSection, WICCreateBitmapFromSection function [Windows Imaging Component], _wic_codec_wiccreatebitmapfromsection, wic._wic_codec_wiccreatebitmapfromsection, wincodec/WICCreateBitmapFromSection
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICCreateBitmapFromSection
 - wincodec/WICCreateBitmapFromSection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Windowscodecs.dll
 - Windowscodecs.lib
api_name:
 - WICCreateBitmapFromSection
---

# WICCreateBitmapFromSection function


## -description

Returns a <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> that is backed by the pixels of a Windows Graphics Device Interface (GDI) section handle.

## -parameters

### -param width [in]

Type: <b>UINT</b>

The width of the bitmap pixels.

### -param height [in]

Type: <b>UINT</b>

The height of the bitmap pixels.

### -param pixelFormat

Type: <b><a href="/windows/desktop/wic/-wic-codec-native-pixel-formats">REFWICPixelFormatGUID</a></b>

The pixel format of the bitmap.

### -param hSection [in]

Type: <b>HANDLE</b>

The section handle. This is a file mapping object handle returned by the <a href="/windows/desktop/api/winbase/nf-winbase-createfilemappinga">CreateFileMapping</a> function.

### -param stride [in]

Type: <b>UINT</b>

The byte count of each scanline.

### -param offset [in]

Type: <b>UINT</b>

The offset into the section.

### -param ppIBitmap [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a>**</b>

A pointer that receives the bitmap.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>WICCreateBitmapFromSection</b> function calls the <a href="/windows/desktop/api/wincodec/nf-wincodec-wiccreatebitmapfromsectionex">WICCreateBitmapFromSectionEx</a> function with the <i>desiredAccessLevel</i> parameter set to <b>WICSectionAccessLevelRead</b>.
