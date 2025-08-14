---
UID: NF:vfw.ICDrawOpen
title: ICDrawOpen macro (vfw.h)
description: The ICDrawOpen macro opens a driver that can draw images with the specified format.
helpviewer_keywords: ["ICDrawOpen","ICDrawOpen macro [Windows Multimedia]","_win32_ICDrawOpen","multimedia.icdrawopen","vfw/ICDrawOpen"]
old-location: multimedia\icdrawopen.htm
tech.root: Multimedia
ms.assetid: b625a5f7-8212-4339-a1a6-37736def40a0
ms.date: 07/01/2025
ms.keywords: ICDrawOpen, ICDrawOpen macro [Windows Multimedia], _win32_ICDrawOpen, multimedia.icdrawopen, vfw/ICDrawOpen
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
 - ICDrawOpen
 - vfw/ICDrawOpen
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
 - ICDrawOpen
---

# ICDrawOpen macro

## -syntax

```cpp
HIC ICDrawOpen(
    DWORD fccType,
    DWORD fccHandler,
    LPBITMAPINFOHEADER lpbiIn
);
```

## -returns

Type: **HIC**

Returns a handle of a driver if successful or zero otherwise.


## -description

The <b>ICDrawOpen</b> macro opens a driver that can draw images with the specified format.

## -parameters

### -param fccType

Four-character code indicating the type of driver to open. For video streams, the value of this parameter is "VIDC" or ICTYPE_VIDEO.

### -param fccHandler

Four-character code indicating the preferred stream handler to use. Typically, this information is stored in the stream header in an AVI file.

### -param lpbiIn

Pointer to the structure defining the input format. A driver handle will not be returned unless it can decompress this format. For images, this parameter refers to a <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure.

## -remarks

The <b>ICDrawOpen</b> macro is defined as follows:


```cpp

#define ICDrawOpen(fccType, fccHandler, lpbiIn) \
    ICLocate(fccType, fccHandler, lpbiIn, NULL, ICMODE_DRAW); 

```

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
