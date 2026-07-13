---
UID: NF:vfw.ICCompressGetFormatSize
title: ICCompressGetFormatSize macro (vfw.h)
description: The ICCompressGetFormatSize macro requests the size of the output format of the compressed data from a video compression driver. You can use this macro or explicitly call the ICM_COMPRESS_GET_FORMAT message.
helpviewer_keywords: ["ICCompressGetFormatSize","ICCompressGetFormatSize macro [Windows Multimedia]","_win32_ICCompressGetFormatSize","multimedia.iccompressgetformatsize","vfw/ICCompressGetFormatSize"]
old-location: multimedia\iccompressgetformatsize.htm
tech.root: Multimedia
ms.assetid: 50d73009-1f8e-4e2e-950c-0c1262ea61f0
ms.date: 07/01/2025
ms.keywords: ICCompressGetFormatSize, ICCompressGetFormatSize macro [Windows Multimedia], _win32_ICCompressGetFormatSize, multimedia.iccompressgetformatsize, vfw/ICCompressGetFormatSize
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
 - ICCompressGetFormatSize
 - vfw/ICCompressGetFormatSize
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
 - ICCompressGetFormat
---

# ICCompressGetFormatSize macro

## -syntax

```cpp
DWORD ICCompressGetFormat(
     hic,
     lpbi
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns the size of the structure.


## -description

The <b>ICCompressGetFormatSize</b> macro requests the size of the output format of the compressed data from a video compression driver. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-compress-get-format">ICM_COMPRESS_GET_FORMAT</a> message.

## -parameters

### -param hic

Handle of the compressor.

### -param lpbi

Pointer to a <b>BITMAPINFO</b> structure containing the input format.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
