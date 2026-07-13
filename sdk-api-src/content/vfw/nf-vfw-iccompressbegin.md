---
UID: NF:vfw.ICCompressBegin
title: ICCompressBegin macro (vfw.h)
description: The ICCompressBegin macro notifies a video compression driver to prepare to compress data. You can use this macro or explicitly call the ICM_COMPRESS_BEGIN message.
helpviewer_keywords: ["ICCompressBegin","ICCompressBegin macro [Windows Multimedia]","_win32_ICCompressBegin","multimedia.iccompressbegin","vfw/ICCompressBegin"]
old-location: multimedia\iccompressbegin.htm
tech.root: Multimedia
ms.assetid: e09d3ac8-ead3-459c-a773-ffbe8198b40f
ms.date: 07/01/2025
ms.keywords: ICCompressBegin, ICCompressBegin macro [Windows Multimedia], _win32_ICCompressBegin, multimedia.iccompressbegin, vfw/ICCompressBegin
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
 - ICCompressBegin
 - vfw/ICCompressBegin
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
 - ICCompressBegin
---

# ICCompressBegin macro

## -syntax

```cpp
DWORD ICCompressBegin(
     hic,
     lpbiInput,
     lpbiOutput
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns ICERR_OK if the specified compression is supported or ICERR_BADFORMAT if the input or output format is not supported.


## -description

The ICCompressBegin macro notifies a video compression driver to prepare to compress data. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-compress-begin">ICM_COMPRESS_BEGIN</a> message.

## -parameters

### -param hic

Handle to a compressor.

### -param lpbiInput

Pointer to a <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFO</a> structure containing the input format.

### -param lpbiOutput

Pointer to a <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFO</a> structure containing the output format.

## -remarks

The driver should allocate and initialize any tables or memory that it needs for compressing the data formats when it receives the <a href="/windows/desktop/Multimedia/icm-compress">ICM_COMPRESS</a> message.

VCM saves the settings of the most recent <b>ICCompressBegin</b> macro. The <b>ICCompressBegin</b> and <b>ICCompressEnd</b> messages do not nest. If your driver receives <b>ICM_COMPRESS_BEGIN</b> before compression is stopped with <b>ICM_COMPRESS_END</b>, it should restart compression with new parameters.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
