---
UID: NF:vfw.ICDrawRenderBuffer
title: ICDrawRenderBuffer macro (vfw.h)
description: The ICDrawRenderBuffer macro notifies a rendering driver to draw the frames that have been passed to it. You can use this macro or explicitly call the ICM_DRAW_RENDERBUFFER message.
helpviewer_keywords: ["ICDrawRenderBuffer","ICDrawRenderBuffer macro [Windows Multimedia]","_win32_ICDrawRenderBuffer","multimedia.icdrawrenderbuffer","vfw/ICDrawRenderBuffer"]
old-location: multimedia\icdrawrenderbuffer.htm
tech.root: Multimedia
ms.assetid: dc87dd00-1a48-4434-894c-fb49d4e92d20
ms.date: 12/05/2018
ms.keywords: ICDrawRenderBuffer, ICDrawRenderBuffer macro [Windows Multimedia], _win32_ICDrawRenderBuffer, multimedia.icdrawrenderbuffer, vfw/ICDrawRenderBuffer
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
 - ICDrawRenderBuffer
 - vfw/ICDrawRenderBuffer
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
 - ICDrawRenderBuffer
---

# ICDrawRenderBuffer macro


## -description

The <b>ICDrawRenderBuffer</b> macro notifies a rendering driver to draw the frames that have been passed to it. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-draw-renderbuffer">ICM_DRAW_RENDERBUFFER</a> message.

## -parameters

### -param hic

Handle to a driver.

## -remarks

Use this message with hardware that performs its own asynchronous decompression, timing, and drawing.

This message is typically used to perform a seek operation when the driver must be specifically instructed to display each video frame passed to it rather than playing a sequence of video frames.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>