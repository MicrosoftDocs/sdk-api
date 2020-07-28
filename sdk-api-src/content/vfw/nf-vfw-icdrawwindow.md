---
UID: NF:vfw.ICDrawWindow
title: ICDrawWindow macro (vfw.h)
description: The ICDrawWindow macro notifies a rendering driver that the window specified for the ICM_DRAW_BEGIN message needs to be redrawn. The window has moved or become temporarily obscured. You can use this macro or explicitly call the ICM_DRAW_WINDOW message.
helpviewer_keywords: ["ICDrawWindow","ICDrawWindow macro [Windows Multimedia]","_win32_ICDrawWindow","multimedia.icdrawwindow","vfw/ICDrawWindow"]
old-location: multimedia\icdrawwindow.htm
tech.root: Multimedia
ms.assetid: 35f799f6-99ce-41a4-9165-3bb614ea01d5
ms.date: 12/05/2018
ms.keywords: ICDrawWindow, ICDrawWindow macro [Windows Multimedia], _win32_ICDrawWindow, multimedia.icdrawwindow, vfw/ICDrawWindow
f1_keywords:
- vfw/ICDrawWindow
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Vfw.h
api_name:
- ICDrawWindow
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICDrawWindow macro


## -description



The <b>ICDrawWindow</b> macro notifies a rendering driver that the window specified for the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-draw-begin">ICM_DRAW_BEGIN</a> message needs to be redrawn. The window has moved or become temporarily obscured. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-draw-window">ICM_DRAW_WINDOW</a> message.




## -parameters




### -param hic

Handle to a driver. 


### -param prc

Pointer to the destination rectangle in screen coordinates. If this parameter points to an empty rectangle, drawing should be turned off. 


## -remarks



This message is supported by hardware that performs its own asynchronous decompression, timing, and drawing.

Video-overlay drivers use this message to draw when the window is obscured or moved. When a window specified for <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-draw-begin">ICM_DRAW_BEGIN</a> is completely hidden by other windows, the destination rectangle is empty. Drivers should turn off video-overlay hardware when this condition occurs.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
 

 

