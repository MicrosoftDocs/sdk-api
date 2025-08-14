---
UID: NF:vfw.ICDrawFlush
title: ICDrawFlush macro (vfw.h)
description: The ICDrawFlush macro notifies a rendering driver to render the contents of any image buffers that are waiting to be drawn. You can use this macro or explicitly call the ICM_DRAW_FLUSH message.
helpviewer_keywords: ["ICDrawFlush","ICDrawFlush macro [Windows Multimedia]","_win32_ICDrawFlush","multimedia.icdrawflush","vfw/ICDrawFlush"]
old-location: multimedia\icdrawflush.htm
tech.root: Multimedia
ms.assetid: ceff1075-4e23-4be0-aac0-27fc5fe68083
ms.date: 07/01/2025
ms.keywords: ICDrawFlush, ICDrawFlush macro [Windows Multimedia], _win32_ICDrawFlush, multimedia.icdrawflush, vfw/ICDrawFlush
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
 - ICDrawFlush
 - vfw/ICDrawFlush
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
 - ICDrawFlush
---

# ICDrawFlush macro

## -syntax

```cpp
DWORD ICDrawFlush(
     hic
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns ICERR_OK if successful or an error otherwise.


## -description

The <b>ICDrawFlush</b> macro notifies a rendering driver to render the contents of any image buffers that are waiting to be drawn. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-draw-flush">ICM_DRAW_FLUSH</a> message.

## -parameters

### -param hic

Handle to a driver.

## -remarks

This message is used only by hardware that performs its own asynchronous decompression, timing, and drawing.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
