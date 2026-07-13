---
UID: NF:vfw.ICCompressGetFormat
title: ICCompressGetFormat macro (vfw.h)
description: The ICCompressGetFormat macro requests the output format of the compressed data from a video compression driver. You can use this macro or explicitly call the ICM_COMPRESS_GET_FORMAT message.
helpviewer_keywords: ["ICCompressGetFormat","ICCompressGetFormat macro [Windows Multimedia]","_win32_ICCompressGetFormat","multimedia.iccompressgetformat","vfw/ICCompressGetFormat"]
old-location: multimedia\iccompressgetformat.htm
tech.root: Multimedia
ms.assetid: d6552dc0-21fb-475c-9ec4-cb3ef1f3a70e
ms.date: 07/01/2025
ms.keywords: ICCompressGetFormat, ICCompressGetFormat macro [Windows Multimedia], _win32_ICCompressGetFormat, multimedia.iccompressgetformat, vfw/ICCompressGetFormat
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
 - ICCompressGetFormat
 - vfw/ICCompressGetFormat
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

# ICCompressGetFormat macro

## -syntax

```cpp
DWORD ICCompressGetFormat(
     hic,
     lpbiInput,
     lpbiOutput
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

If _lpbiOutput_ is zero, returns the size of the structure. If _lpbiOutput_ is nonzero, returns ICERR_OK if successful or an error otherwise.


## -description

The <b>ICCompressGetFormat</b> macro requests the output format of the compressed data from a video compression driver. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-compress-get-format">ICM_COMPRESS_GET_FORMAT</a> message.

## -parameters

### -param hic

Handle of the compressor.

### -param lpbiInput

Pointer to a BITMAPINFO structure containing the input format.

### -param lpbiOutput

Pointer to a BITMAPINFO structure containing the output format.

## -remarks

If <i>lpbiOutput</i> is nonzero, the driver should fill the <b>BITMAPINFO</b> structure with the default output format corresponding to the input format specified for <i>lpbiInput</i>. If the compressor can produce several formats, the default format should be the one that preserves the greatest amount of information.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
