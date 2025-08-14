---
UID: NF:vfw.ICDecompressEnd
title: ICDecompressEnd macro (vfw.h)
description: The ICDecompressEnd macro notifies a video decompression driver to end decompression and free resources allocated for decompression. You can use this macro or explicitly call the ICM_DECOMPRESS_END message.
helpviewer_keywords: ["ICDecompressEnd","ICDecompressEnd macro [Windows Multimedia]","_win32_ICDecompressEnd","multimedia.icdecompressend","vfw/ICDecompressEnd"]
old-location: multimedia\icdecompressend.htm
tech.root: Multimedia
ms.assetid: 9d66174a-b6bd-4bcd-a88a-bb1876bbc510
ms.date: 07/01/2025
ms.keywords: ICDecompressEnd, ICDecompressEnd macro [Windows Multimedia], _win32_ICDecompressEnd, multimedia.icdecompressend, vfw/ICDecompressEnd
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
 - ICDecompressEnd
 - vfw/ICDecompressEnd
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
 - ICDecompressEnd
---

# ICDecompressEnd macro

## -syntax

```cpp
DWORD ICDecompressEnd(
     hic
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns ICERR_OK if successful or an error otherwise.


## -description

The <b>ICDecompressEnd</b> macro notifies a video decompression driver to end decompression and free resources allocated for decompression. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-decompress-end">ICM_DECOMPRESS_END</a> message.

## -parameters

### -param hic

Handle to a decompressor.

## -remarks

The driver should free any resources allocated for the <a href="/windows/desktop/Multimedia/icm-decompress-begin">ICM_DECOMPRESS_BEGIN</a> message.

The <a href="/windows/desktop/api/vfw/nf-vfw-icdecompressbegin">ICDecompressBegin</a> and <b>ICDecompressEnd</b> macros do not nest. If your driver receives <a href="/windows/desktop/Multimedia/icm-decompress-begin">ICM_DECOMPRESS_BEGIN</a> before decompression is stopped with <a href="/windows/desktop/Multimedia/icm-decompress-end">ICM_DECOMPRESS_END</a>, it should restart decompression with new parameters.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
