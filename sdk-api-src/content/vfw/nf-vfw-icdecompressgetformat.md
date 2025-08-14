---
UID: NF:vfw.ICDecompressGetFormat
title: ICDecompressGetFormat macro (vfw.h)
description: The ICDecompressGetFormat macro requests the output format of the decompressed data from a video decompression driver. You can use this macro or explicitly call the ICM_DECOMPRESS_GET_FORMAT message.
helpviewer_keywords: ["ICDecompressGetFormat","ICDecompressGetFormat macro [Windows Multimedia]","_win32_ICDecompressGetFormat","multimedia.icdecompressgetformat","vfw/ICDecompressGetFormat"]
old-location: multimedia\icdecompressgetformat.htm
tech.root: Multimedia
ms.assetid: c45ff664-03f0-4cda-9ffd-fb7ea2656e43
ms.date: 07/01/2025
ms.keywords: ICDecompressGetFormat, ICDecompressGetFormat macro [Windows Multimedia], _win32_ICDecompressGetFormat, multimedia.icdecompressgetformat, vfw/ICDecompressGetFormat
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
 - ICDecompressGetFormat
 - vfw/ICDecompressGetFormat
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
 - ICDecompressGetFormat
---

# ICDecompressGetFormat macro

## -syntax

```cpp
DWORD ICDecompressGetFormat(
     hic,
     lpbiInput,
     lpbiOutput
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

If _lpbiOutput_ is zero, returns the size of the structure.If _lpbiOutput_ is nonzero, returns ICERR_OK if successful or an error otherwise.


## -description

The <b>ICDecompressGetFormat</b> macro requests the output format of the decompressed data from a video decompression driver. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-decompress-get-format">ICM_DECOMPRESS_GET_FORMAT</a> message.

## -parameters

### -param hic

Handle to a decompressor.

### -param lpbiInput

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure containing the input format.

### -param lpbiOutput

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure to contain the output format. You can specify zero to request only the size of the output format, as in the <a href="/windows/desktop/api/vfw/nf-vfw-icdecompressgetformatsize">ICDecompressGetFormatSize</a> macro.

## -remarks

If <i>lpbiOutput</i> is nonzero, the driver should fill the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure with the default output format corresponding to the input format specified for <i>lpbiInput</i>. If the compressor can produce several formats, the default format should be the one that preserves the greatest amount of information.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
