---
UID: NF:vfw.ICDecompressQuery
title: ICDecompressQuery macro (vfw.h)
description: The ICDecompressQuery macro queries a video decompression driver to determine if it supports a specific input format or if it can decompress a specific input format to a specific output format.
helpviewer_keywords: ["ICDecompressQuery","ICDecompressQuery macro [Windows Multimedia]","_win32_ICDecompressQuery","multimedia.icdecompressquery","vfw/ICDecompressQuery"]
old-location: multimedia\icdecompressquery.htm
tech.root: Multimedia
ms.assetid: 77d9a28c-dff9-4ccb-a0b8-9dc38fc66372
ms.date: 07/01/2025
ms.keywords: ICDecompressQuery, ICDecompressQuery macro [Windows Multimedia], _win32_ICDecompressQuery, multimedia.icdecompressquery, vfw/ICDecompressQuery
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
 - ICDecompressQuery
 - vfw/ICDecompressQuery
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
 - ICDecompressQuery
---

# ICDecompressQuery macro

## -syntax

```cpp
DWORD ICDecompressQuery(
     hic,
     lpbiInput,
     lpbiOutput
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns ICERR_OK if the specified decompression is supported or ICERR_BADFORMAT otherwise.


## -description

The <b>ICDecompressQuery</b> macro queries a video decompression driver to determine if it supports a specific input format or if it can decompress a specific input format to a specific output format. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-decompress-query">ICM_DECOMPRESS_QUERY</a> message.

## -parameters

### -param hic

Handle to a decompressor.

### -param lpbiInput

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure containing the input format.

### -param lpbiOutput

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure containing the output format. You can specify zero for this parameter to indicate any output format is acceptable.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
