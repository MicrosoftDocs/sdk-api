---
UID: NF:vfw.ICDecompressOpen
title: ICDecompressOpen macro (vfw.h)
description: The ICDecompressOpen macro opens a decompressor that is compatible with the specified formats.
helpviewer_keywords: ["ICDecompressOpen","ICDecompressOpen macro [Windows Multimedia]","_win32_ICDecompressOpen","multimedia.icdecompressopen","vfw/ICDecompressOpen"]
old-location: multimedia\icdecompressopen.htm
tech.root: Multimedia
ms.assetid: 83db0e07-7e93-4c77-a017-68a30b1372ef
ms.date: 07/01/2025
ms.keywords: ICDecompressOpen, ICDecompressOpen macro [Windows Multimedia], _win32_ICDecompressOpen, multimedia.icdecompressopen, vfw/ICDecompressOpen
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
 - ICDecompressOpen
 - vfw/ICDecompressOpen
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
 - ICDecompressOpen
---

# ICDecompressOpen macro

## -syntax

```cpp
HIC ICDecompressOpen(
    DWORD fccType,
    DWORD fccHandler,
    LPBITMAPINFOHEADER lpbiIn,
    LPBITMAPINFOHEADER lpbiOut
);
```

## -returns

Type: **HIC**

Returns a handle of a decompressor if successful or zero otherwise.


## -description

The <b>ICDecompressOpen</b> macro opens a decompressor that is compatible with the specified formats.

## -parameters

### -param fccType

Four-character code indicating the type of compressor to open. For video streams, the value of this parameter is "VIDC" or ICTYPE_VIDEO.

### -param fccHandler

Four-character code indicating the preferred stream handler to use. Typically, this information is stored in the stream header in an AVI file.

### -param lpbiIn

Pointer to a structure defining the input format. A decompressor handle is not returned unless it can decompress this format. For bitmaps, this parameter refers to a BITMAPINFOHEADER structure.

### -param lpbiOut

Pointer to a structure defining an optional decompression format. You can also specify zero to use the default output format associated with the input format. 

If this parameter is nonzero, a compressor handle is not returned unless it can create this output format. For bitmaps, this parameter refers to a BITMAPINFOHEADER structure.

## -remarks

The <b>ICDecompressOpen</b> macro is defined as follows:


```cpp

#define ICDecompressOpen(fccType, fccHandler, lpbiIn, lpbiOut) \ 
    ICLocate(fccType, fccHandler, lpbiIn, lpbiOut, ICMODE_DECOMPRESS); 

```

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
