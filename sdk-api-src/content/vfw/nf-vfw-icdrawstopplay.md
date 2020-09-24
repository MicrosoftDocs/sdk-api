---
UID: NF:vfw.ICDrawStopPlay
title: ICDrawStopPlay macro (vfw.h)
description: The ICDrawStopPlay macro notifies a rendering driver when a play operation is complete. You can use this macro or explicitly call the ICM_DRAW_STOP_PLAY message.
helpviewer_keywords: ["ICDrawStopPlay","ICDrawStopPlay macro [Windows Multimedia]","_win32_ICDrawStopPlay","multimedia.icdrawstopplay","vfw/ICDrawStopPlay"]
old-location: multimedia\icdrawstopplay.htm
tech.root: Multimedia
ms.assetid: 41faa7cd-13c9-47bc-a62e-c09c7d3264d7
ms.date: 12/05/2018
ms.keywords: ICDrawStopPlay, ICDrawStopPlay macro [Windows Multimedia], _win32_ICDrawStopPlay, multimedia.icdrawstopplay, vfw/ICDrawStopPlay
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
 - ICDrawStopPlay
 - vfw/ICDrawStopPlay
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
 - ICDrawStopPlay
---

# ICDrawStopPlay macro


## -description

The <b>ICDrawStopPlay</b> macro notifies a rendering driver when a play operation is complete. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-draw-stop-play">ICM_DRAW_STOP_PLAY</a> message.

## -parameters

### -param hic

Handle to a driver.

## -remarks

Use this message when the play operation is complete. Use the <a href="/windows/desktop/api/vfw/nf-vfw-icdrawstop">ICDrawStop</a> macro to end timing.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>