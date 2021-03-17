---
UID: NF:vfw.ICDrawStop
title: ICDrawStop macro (vfw.h)
description: The ICDrawStop macro notifies a rendering driver to stop its internal clock for the timing of drawing frames. You can use this macro or explicitly call the ICM_DRAW_STOP message.
helpviewer_keywords: ["ICDrawStop","ICDrawStop macro [Windows Multimedia]","_win32_ICDrawStop","multimedia.icdrawstop","vfw/ICDrawStop"]
old-location: multimedia\icdrawstop.htm
tech.root: Multimedia
ms.assetid: c8608410-da45-4953-b16a-050870f85af9
ms.date: 12/05/2018
ms.keywords: ICDrawStop, ICDrawStop macro [Windows Multimedia], _win32_ICDrawStop, multimedia.icdrawstop, vfw/ICDrawStop
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
 - ICDrawStop
 - vfw/ICDrawStop
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
 - ICDrawStop
---

# ICDrawStop macro


## -description

The <b>ICDrawStop</b> macro notifies a rendering driver to stop its internal clock for the timing of drawing frames. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-draw-stop">ICM_DRAW_STOP</a> message.

## -parameters

### -param hic

Handle to a driver.

## -remarks

This macro is used by hardware that performs its own asynchronous decompression, timing, and drawing.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>