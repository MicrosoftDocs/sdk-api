---
UID: NF:vfw.ICDecompressBegin
title: ICDecompressBegin macro (vfw.h)
description: The ICDecompressBegin macro notifies a video decompression driver to prepare to decompress data. You can use this macro or explicitly call the ICM_DECOMPRESS_BEGIN message.
helpviewer_keywords: ["ICDecompressBegin","ICDecompressBegin macro [Windows Multimedia]","_win32_ICDecompressBegin","multimedia.icdecompressbegin","vfw/ICDecompressBegin"]
old-location: multimedia\icdecompressbegin.htm
tech.root: Multimedia
ms.assetid: 3e9fb4b7-bdc6-402c-a5c6-3f837149c291
ms.date: 07/01/2025
ms.keywords: ICDecompressBegin, ICDecompressBegin macro [Windows Multimedia], _win32_ICDecompressBegin, multimedia.icdecompressbegin, vfw/ICDecompressBegin
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
 - ICDecompressBegin
 - vfw/ICDecompressBegin
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
 - ICDecompressBegin
---

# ICDecompressBegin macro

## -syntax

```cpp
DWORD ICDecompressBegin(
     hic,
     lpbiInput,
     lpbiOutput
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns ICERR_OK if the specified decompression is supported or ICERR_BADFORMAT otherwise.


## -description

The <b>ICDecompressBegin</b> macro notifies a video decompression driver to prepare to decompress data. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-decompress-begin">ICM_DECOMPRESS_BEGIN</a> message.

## -parameters

### -param hic

Handle to a decompressor.

### -param lpbiInput

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure containing the input format.

### -param lpbiOutput

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure containing the output format.

## -remarks

When the driver receives this message, it should allocate buffers and do any time-consuming operations so that it can process <a href="/windows/desktop/Multimedia/icm-decompress">ICM_DECOMPRESS</a> messages efficiently.

The <b>ICDecompressBegin</b> and <a href="/windows/desktop/api/vfw/nf-vfw-icdecompressend">ICDecompressEnd</a> macros do not nest. If your driver receives <a href="/windows/desktop/Multimedia/icm-decompress-begin">ICM_DECOMPRESS_BEGIN</a> before decompression is stopped with <a href="/windows/desktop/Multimedia/icm-decompress-end">ICM_DECOMPRESS_END</a>, it should restart decompression with new parameters.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
