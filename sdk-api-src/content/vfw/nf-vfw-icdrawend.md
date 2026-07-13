---
UID: NF:vfw.ICDrawEnd
title: ICDrawEnd macro (vfw.h)
description: The ICDrawEnd macro notifies a rendering driver to decompress the current image to the screen and to release resources allocated for decompression and drawing. You can use this macro or explicitly call the ICM_DRAW_END message.
helpviewer_keywords: ["ICDrawEnd","ICDrawEnd macro [Windows Multimedia]","_win32_ICDrawEnd","multimedia.icdrawend","vfw/ICDrawEnd"]
old-location: multimedia\icdrawend.htm
tech.root: Multimedia
ms.assetid: efcb1913-edaf-454c-a317-c14349805a81
ms.date: 07/01/2025
ms.keywords: ICDrawEnd, ICDrawEnd macro [Windows Multimedia], _win32_ICDrawEnd, multimedia.icdrawend, vfw/ICDrawEnd
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
 - ICDrawEnd
 - vfw/ICDrawEnd
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
 - ICDrawEnd
---

# ICDrawEnd macro

## -syntax

```cpp
DWORD ICDrawEnd(
     hic
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns ICERR_OK if successful or an error otherwise.


## -description

The <b>ICDrawEnd</b> macro notifies a rendering driver to decompress the current image to the screen and to release resources allocated for decompression and drawing. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-draw-end">ICM_DRAW_END</a> message.

## -parameters

### -param hic

Handle to a driver.

## -remarks

The <a href="/windows/desktop/Multimedia/icm-draw-begin">ICM_DRAW_BEGIN</a> and <a href="/windows/desktop/Multimedia/icm-draw-end">ICM_DRAW_END</a> messages do not nest. If your driver receives <b>ICM_DRAW_BEGIN</b> before decompression is stopped with <b>ICM_DRAW_END</b>, it should restart decompression with new parameters.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
