---
UID: NF:vfw.ICImageDecompress
title: ICImageDecompress function (vfw.h)
description: The ICImageDecompress function decompresses an image without using initialization functions.
helpviewer_keywords: ["ICImageDecompress","ICImageDecompress function [Windows Multimedia]","_win32_ICImageDecompress","multimedia.icimagedecompress","vfw/ICImageDecompress"]
old-location: multimedia\icimagedecompress.htm
tech.root: Multimedia
ms.assetid: 8d27f0bd-9db5-482d-9000-75ad04762a67
ms.date: 12/05/2018
ms.keywords: ICImageDecompress, ICImageDecompress function [Windows Multimedia], _win32_ICImageDecompress, multimedia.icimagedecompress, vfw/ICImageDecompress
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
 - ICImageDecompress
 - vfw/ICImageDecompress
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
 - ICImageDecompress
---

# ICImageDecompress function


## -description

The <b>ICImageDecompress</b> function decompresses an image without using initialization functions.

## -parameters

### -param hic

Handle to a decompressor opened with the <a href="/windows/desktop/api/vfw/nf-vfw-icopen">ICOpen</a> function. Specify <b>NULL</b> to have VCM select an appropriate decompressor for the compressed image.

### -param uiFlags

Reserved; must be zero.

### -param lpbiIn

Compressed input data format.

### -param lpBits

Pointer to input data bits to compress. The data bits exclude header and format information.

### -param lpbiOut

Decompressed output format. Specify <b>NULL</b> to let decompressor use an appropriate format.

## -returns

Returns a handle to an uncompressed DIB in the CF_DIB format if successful or <b>NULL</b> otherwise. Image data follows the format header.

## -remarks

To obtain the format information from the <b>LPBITMAPINFOHEADER</b> structure, use the <b>GlobalLock</b> function to lock the data. Use the <b>GlobalFree</b> function to free the DIB when you are finished.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>