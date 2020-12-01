---
UID: NF:vfw.ICGetDisplayFormat
title: ICGetDisplayFormat function (vfw.h)
description: The ICGetDisplayFormat function determines the best format available for displaying a compressed image. The function also opens a compressor if a handle of an open compressor is not specified.
helpviewer_keywords: ["ICGetDisplayFormat","ICGetDisplayFormat function [Windows Multimedia]","_win32_ICGetDisplayFormat","multimedia.icgetdisplayformat","vfw/ICGetDisplayFormat"]
old-location: multimedia\icgetdisplayformat.htm
tech.root: Multimedia
ms.assetid: 4e588524-4105-4496-bc87-407abc45f598
ms.date: 12/05/2018
ms.keywords: ICGetDisplayFormat, ICGetDisplayFormat function [Windows Multimedia], _win32_ICGetDisplayFormat, multimedia.icgetdisplayformat, vfw/ICGetDisplayFormat
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
 - ICGetDisplayFormat
 - vfw/ICGetDisplayFormat
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
 - ICGetDisplayFormat
---

# ICGetDisplayFormat function


## -description

The <b>ICGetDisplayFormat</b> function determines the best format available for displaying a compressed image. The function also opens a compressor if a handle of an open compressor is not specified.

## -parameters

### -param hic

Handle to the compressor to use. Specify <b>NULL</b> to have VCM select and open an appropriate compressor.

### -param lpbiIn

Pointer to <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure containing the compressed format.

### -param lpbiOut

Pointer to a buffer to return the decompressed format. The buffer should be large enough for a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure and 256 color entries.

### -param BitDepth

Preferred bit depth, if nonzero.

### -param dx

Width multiplier to stretch the image. If this parameter is zero, that dimension is not stretched.

### -param dy

Height multiplier to stretch the image. If this parameter is zero, that dimension is not stretched.

## -returns

Returns a handle to a decompressor if successful or zero otherwise.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>