---
UID: NF:vfw.ICDrawSetTime
title: ICDrawSetTime macro (vfw.h)
description: The ICDrawSetTime macro provides synchronization information to a rendering driver that handles the timing of drawing frames.
helpviewer_keywords: ["ICDrawSetTime","ICDrawSetTime macro [Windows Multimedia]","_win32_ICDrawSetTime","multimedia.icdrawsettime","vfw/ICDrawSetTime"]
old-location: multimedia\icdrawsettime.htm
tech.root: Multimedia
ms.assetid: 4c97e0ee-c6f1-4258-9a5f-de633f8c0335
ms.date: 07/01/2025
ms.keywords: ICDrawSetTime, ICDrawSetTime macro [Windows Multimedia], _win32_ICDrawSetTime, multimedia.icdrawsettime, vfw/ICDrawSetTime
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
 - ICDrawSetTime
 - vfw/ICDrawSetTime
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
 - ICDrawSetTime
---

# ICDrawSetTime macro

## -syntax

```cpp
DWORD ICDrawSetTime(
     hic,
     lTime
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns ICERR_OK if successful or an error otherwise.


## -description

The <b>ICDrawSetTime</b> macro provides synchronization information to a rendering driver that handles the timing of drawing frames. The synchronization information is the sample number of the frame to draw. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/icm-draw-settime">ICM_DRAW_SETTIME</a> message.

## -parameters

### -param hic

Handle to a driver.

### -param lTime

Sample number of the frame to render.

## -remarks

Typically, the driver compares the specified value with the frame number associated with the time of its internal clock and attempts to synchronize the two if the difference is significant.

Use this message when the hardware performs its own asynchronous decompression, timing, and drawing, and the hardware relies on an external synchronization signal (the hardware is not being used as the synchronization master).

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
