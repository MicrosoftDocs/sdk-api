---
UID: NF:vfw.ICCompressGetSize
title: ICCompressGetSize macro (vfw.h)
description: The ICCompressGetSize macro requests that the video compression driver supply the maximum size of one frame of data when compressed into the specified output format. You can use this macro or explicitly call the ICM_COMPRESS_GET_SIZE message.
helpviewer_keywords: ["ICCompressGetSize","ICCompressGetSize macro [Windows Multimedia]","_win32_ICCompressGetSize","multimedia.iccompressgetsize","vfw/ICCompressGetSize"]
old-location: multimedia\iccompressgetsize.htm
tech.root: Multimedia
ms.assetid: 6cb85b0b-4a05-44f7-af61-303a94b49847
ms.date: 07/01/2025
ms.keywords: ICCompressGetSize, ICCompressGetSize macro [Windows Multimedia], _win32_ICCompressGetSize, multimedia.iccompressgetsize, vfw/ICCompressGetSize
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICCompressGetSize
 - vfw/ICCompressGetSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - ICCompressGetSize
---

# ICCompressGetSize macro

## -syntax

```cpp
DWORD ICCompressGetSize(
     hic,
     lpbiInput,
     lpbiOutput
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns the maximum number of bytes a single compressed frame can occupy.


## -description

The <b>ICCompressGetSize</b> macro requests that the video compression driver supply the maximum size of one frame of data when compressed into the specified output format. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-compress-get-size">ICM_COMPRESS_GET_SIZE</a> message.

## -parameters

### -param hic

Handle to a compressor.

### -param lpbiInput

Pointer to a BITMAPINFO structure containing the input format.

### -param lpbiOutput

Pointer to a BITMAPINFO structure containing the output format.

## -remarks

Typically, applications send this message to determine how large a buffer to allocate for the compressed frame.

The driver should calculate the size of the largest possible frame based on the input and output formats.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
