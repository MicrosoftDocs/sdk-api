---
UID: NF:vfw.ICDrawStartPlay
title: ICDrawStartPlay macro (vfw.h)
description: The ICDrawStartPlay macro provides the start and end times of a play operation to a rendering driver. You can use this macro or explicitly call the ICM_DRAW_START_PLAY message.
helpviewer_keywords: ["ICDrawStartPlay","ICDrawStartPlay macro [Windows Multimedia]","_win32_ICDrawStartPlay","multimedia.icdrawstartplay","vfw/ICDrawStartPlay"]
old-location: multimedia\icdrawstartplay.htm
tech.root: Multimedia
ms.assetid: 74957f08-2912-4e5e-af45-7dc66b405bc2
ms.date: 12/05/2018
ms.keywords: ICDrawStartPlay, ICDrawStartPlay macro [Windows Multimedia], _win32_ICDrawStartPlay, multimedia.icdrawstartplay, vfw/ICDrawStartPlay
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
 - ICDrawStartPlay
 - vfw/ICDrawStartPlay
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
 - ICDrawStartPlay
---

# ICDrawStartPlay macro


## -description

The <b>ICDrawStartPlay</b> macro provides the start and end times of a play operation to a rendering driver. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-draw-start-play">ICM_DRAW_START_PLAY</a> message.

## -parameters

### -param hic

Handle to a driver.

### -param lFrom

Start time.

### -param lTo

End time.

## -remarks

This message precedes any frame data sent to the rendering driver.

Units for <i>lFrom</i> and <i>lTo</i> are specified with the <a href="/windows/desktop/Multimedia/icm-draw-begin">ICM_DRAW_BEGIN</a> message. For video data this is normally a frame number. For more information about the playback rate, see the <b>dwRate</b> and <b>dwScale</b> members of the <a href="/windows/desktop/api/vfw/ns-vfw-icdrawbegin">ICDRAWBEGIN</a> structure.

If the end time is less than the start time, the playback direction is reversed.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>