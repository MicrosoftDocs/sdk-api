---
UID: NF:vfw.ICDrawRealize
title: ICDrawRealize macro (vfw.h)
description: The ICDrawRealize macro notifies a rendering driver to realize its drawing palette while drawing. You can use this macro or explicitly call the ICM_DRAW_REALIZE message.
helpviewer_keywords: ["ICDrawRealize","ICDrawRealize macro [Windows Multimedia]","_win32_ICDrawRealize","multimedia.icdrawrealize","vfw/ICDrawRealize"]
old-location: multimedia\icdrawrealize.htm
tech.root: Multimedia
ms.assetid: b6605223-ce66-49fc-bfa7-6e3dd98e214a
ms.date: 07/01/2025
ms.keywords: ICDrawRealize, ICDrawRealize macro [Windows Multimedia], _win32_ICDrawRealize, multimedia.icdrawrealize, vfw/ICDrawRealize
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
 - ICDrawRealize
 - vfw/ICDrawRealize
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
 - ICDrawRealize
---

# ICDrawRealize macro

## -syntax

```cpp
DWORD ICDrawRealize(
     hic,
     hdc,
     fBackground
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns ICERR_OK if the drawing palette is realized or ICERR_UNSUPPORTED if the palette associated with the decompressed data is realized.


## -description

The <b>ICDrawRealize</b> macro notifies a rendering driver to realize its drawing palette while drawing. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-draw-realize">ICM_DRAW_REALIZE</a> message.

## -parameters

### -param hic

Handle to a driver.

### -param hdc

Handle of the DC used to realize the palette.

### -param fBackground

Background flag. Specify <b>TRUE</b> to realize the palette as a background task or <b>FALSE</b> to realize the palette in the foreground.

## -remarks

Drivers need to respond to this message only if the drawing palette is different from the decompressed palette.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
