---
UID: NF:vfw.ICDrawChangePalette
title: ICDrawChangePalette macro (vfw.h)
description: The ICDrawChangePalette macro notifies a rendering driver that the movie palette is changing. You can use this macro or explicitly call the ICM_DRAW_CHANGEPALETTE message.
helpviewer_keywords: ["ICDrawChangePalette","ICDrawChangePalette macro [Windows Multimedia]","_win32_ICDrawChangePalette","multimedia.icdrawchangepalette","vfw/ICDrawChangePalette"]
old-location: multimedia\icdrawchangepalette.htm
tech.root: Multimedia
ms.assetid: 4b280b51-a45f-47e5-b54c-47dc4a6ca81c
ms.date: 07/01/2025
ms.keywords: ICDrawChangePalette, ICDrawChangePalette macro [Windows Multimedia], _win32_ICDrawChangePalette, multimedia.icdrawchangepalette, vfw/ICDrawChangePalette
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
 - ICDrawChangePalette
 - vfw/ICDrawChangePalette
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
 - ICDrawChangePalette
---

# ICDrawChangePalette macro

## -syntax

```cpp
DWORD ICDrawChangePalette(
     hic,
     lpbiInput
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns ICERR_OK if successful or **FALSE** otherwise.


## -description

The <b>ICDrawChangePalette</b> macro notifies a rendering driver that the movie palette is changing. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-draw-changepalette">ICM_DRAW_CHANGEPALETTE</a> message.

## -parameters

### -param hic

Handle to a rendering driver.

### -param lpbiInput

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure containing the new format and optional color table.

## -remarks

This message should be supported by installable rendering handlers that draw DIBs with an internal structure that includes a palette.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
