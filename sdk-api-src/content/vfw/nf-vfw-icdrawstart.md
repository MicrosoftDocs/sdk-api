---
UID: NF:vfw.ICDrawStart
title: ICDrawStart macro (vfw.h)
description: The ICDrawStart macro notifies a rendering driver to start its internal clock for the timing of drawing frames. You can use this macro or explicitly call the ICM_DRAW_START message.
helpviewer_keywords: ["ICDrawStart","ICDrawStart macro [Windows Multimedia]","_win32_ICDrawStart","multimedia.icdrawstart","vfw/ICDrawStart"]
old-location: multimedia\icdrawstart.htm
tech.root: Multimedia
ms.assetid: 00db96a3-d7e4-42eb-929a-c967ac8380d1
ms.date: 12/05/2018
ms.keywords: ICDrawStart, ICDrawStart macro [Windows Multimedia], _win32_ICDrawStart, multimedia.icdrawstart, vfw/ICDrawStart
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
 - ICDrawStart
 - vfw/ICDrawStart
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
 - ICDrawStart
---

# ICDrawStart macro


## -description

The <b>ICDrawStart</b> macro notifies a rendering driver to start its internal clock for the timing of drawing frames. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-draw-start">ICM_DRAW_START</a> message.

## -parameters

### -param hic

Handle to a driver.

## -remarks

This message is used by hardware that performs its own asynchronous decompression, timing, and drawing.

When the driver receives this message, it should start rendering data at the rate specified with the <a href="/windows/desktop/Multimedia/icm-draw-begin">ICM_DRAW_BEGIN</a> message.

The <b>ICDrawStart</b> and <a href="/windows/desktop/api/vfw/nf-vfw-icdrawstop">ICDrawStop</a> macros do not nest. If your driver receives <b>ICDrawStart</b> before rendering is stopped with <b>ICDrawStop</b>, it should restart rendering with new parameters.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>