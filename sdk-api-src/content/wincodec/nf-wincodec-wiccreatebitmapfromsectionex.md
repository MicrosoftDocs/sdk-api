---
UID: NF:wincodec.WICCreateBitmapFromSectionEx
title: WICCreateBitmapFromSectionEx function (wincodec.h)
description: Returns a IWICBitmapSource that is backed by the pixels of a Windows Graphics Device Interface (GDI) section handle. (WICCreateBitmapFromSectionEx)
helpviewer_keywords: ["WICCreateBitmapFromSectionEx","WICCreateBitmapFromSectionEx function [Windows Imaging Component]","_wic_codec_wiccreatebitmapfromsectionex","wic._wic_codec_wiccreatebitmapfromsectionex","wincodec/WICCreateBitmapFromSectionEx"]
old-location: wic\_wic_codec_wiccreatebitmapfromsectionex.htm
tech.root: wic
ms.assetid: 0c9892a5-c136-41f6-8161-8077afe1a9da
ms.date: 12/05/2018
ms.keywords: WICCreateBitmapFromSectionEx, WICCreateBitmapFromSectionEx function [Windows Imaging Component], _wic_codec_wiccreatebitmapfromsectionex, wic._wic_codec_wiccreatebitmapfromsectionex, wincodec/WICCreateBitmapFromSectionEx
req.header: wincodec.h
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
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICCreateBitmapFromSectionEx
 - wincodec/WICCreateBitmapFromSectionEx
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
 - WICCreateBitmapFromSectionEx
---

# WICCreateBitmapFromSectionEx function


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

### -param desiredAccessLevel [in]

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicsectionaccesslevel">WICSectionAccessLevel</a></b>

The desired access level.

### -param ppIBitmap [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a>**</b>

A pointer that receives the bitmap.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
