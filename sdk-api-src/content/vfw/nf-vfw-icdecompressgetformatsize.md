---
UID: NF:vfw.ICDecompressGetFormatSize
title: ICDecompressGetFormatSize macro (vfw.h)
description: The ICDecompressGetFormatSize macro requests the size of the output format of the decompressed data from a video decompression driver. You can use this macro or explicitly call the ICM_DECOMPRESS_GET_FORMAT message.
helpviewer_keywords: ["ICDecompressGetFormatSize","ICDecompressGetFormatSize macro [Windows Multimedia]","_win32_ICDecompressGetFormatSize","multimedia.icdecompressgetformatsize","vfw/ICDecompressGetFormatSize"]
old-location: multimedia\icdecompressgetformatsize.htm
tech.root: Multimedia
ms.assetid: 249a9d02-a51e-46f2-aea4-71460392705f
ms.date: 07/01/2025
ms.keywords: ICDecompressGetFormatSize, ICDecompressGetFormatSize macro [Windows Multimedia], _win32_ICDecompressGetFormatSize, multimedia.icdecompressgetformatsize, vfw/ICDecompressGetFormatSize
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
 - ICDecompressGetFormatSize
 - vfw/ICDecompressGetFormatSize
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
 - ICDecompressGetFormatSize
---

# ICDecompressGetFormatSize macro

## -syntax

```cpp
DWORD ICDecompressGetFormatSize(
     hic,
     lpbi
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns the size of the structure.


## -description

The <b>ICDecompressGetFormatSize</b> macro requests the size of the output format of the decompressed data from a video decompression driver. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-decompress-get-format">ICM_DECOMPRESS_GET_FORMAT</a> message.

## -parameters

### -param hic

Handle to a decompressor.

### -param lpbi

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure containing the input format.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
