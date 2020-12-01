---
UID: NF:vfw.ICImageCompress
title: ICImageCompress function (vfw.h)
description: The ICImageCompress function compresses an image to a given size. This function does not require initialization functions.
helpviewer_keywords: ["ICImageCompress","ICImageCompress function [Windows Multimedia]","_win32_ICImageCompress","multimedia.icimagecompress","vfw/ICImageCompress"]
old-location: multimedia\icimagecompress.htm
tech.root: Multimedia
ms.assetid: 111d3b97-527b-4cca-ba4e-3d8310a5c72b
ms.date: 12/05/2018
ms.keywords: ICImageCompress, ICImageCompress function [Windows Multimedia], _win32_ICImageCompress, multimedia.icimagecompress, vfw/ICImageCompress
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICImageCompress
 - vfw/ICImageCompress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - ICImageCompress
---

# ICImageCompress function


## -description

The <b>ICImageCompress</b> function compresses an image to a given size. This function does not require initialization functions.

## -parameters

### -param hic

Handle to a compressor opened with the <a href="/windows/desktop/api/vfw/nf-vfw-icopen">ICOpen</a> function. Specify <b>NULL</b> to have VCM select an appropriate compressor for the compression format. An application can have the user select the compressor by using the <a href="/windows/desktop/api/vfw/nf-vfw-iccompressorchoose">ICCompressorChoose</a> function, which opens the selected compressor and returns a handle of the compressor in this parameter.

### -param uiFlags

Reserved; must be zero.

### -param lpbiIn

Pointer to the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure containing the input data format.

### -param lpBits

Pointer to input data bits to compress. The data bits exclude header and format information.

### -param lpbiOut

Pointer to the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure containing the compressed output format. Specify <b>NULL</b> to have the compressor use an appropriate format.

### -param lQuality

Quality value used by the compressor. Values range from 0 to 10,000.

### -param plSize

Maximum size desired for the compressed image. The compressor might not be able to compress the data to fit within this size. When the function returns, this parameter points to the size of the compressed image. Image sizes are specified in bytes.

## -returns

Returns a handle to a compressed DIB. The image data follows the format header.

## -remarks

To obtain the format information from the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure, use the <a href="/windows/win32/api/winbase/nf-winbase-globallock">GlobalLock</a> function to lock the data. Use the <a href="/windows/win32/api/winbase/nf-winbase-globalfree">GlobalFree</a> function to free the DIB when you are finished.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>