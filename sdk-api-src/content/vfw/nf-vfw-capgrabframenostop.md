---
UID: NF:vfw.capGrabFrameNoStop
title: capGrabFrameNoStop macro (vfw.h)
description: The capGrabFrameNoStop macro fills the frame buffer with a single uncompressed frame from the capture device and displays it.
helpviewer_keywords: ["_win32_capGrabFrameNoStop","capGrabFrameNoStop","capGrabFrameNoStop macro [Windows Multimedia]","multimedia.capgrabframenostop","vfw/capGrabFrameNoStop"]
old-location: multimedia\capgrabframenostop.htm
tech.root: Multimedia
ms.assetid: 0782d69f-6c4f-44f5-abd4-2b833be2f487
ms.date: 12/05/2018
ms.keywords: _win32_capGrabFrameNoStop, capGrabFrameNoStop, capGrabFrameNoStop macro [Windows Multimedia], multimedia.capgrabframenostop, vfw/capGrabFrameNoStop
f1_keywords:
- vfw/capGrabFrameNoStop
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
- capGrabFrameNoStop
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capGrabFrameNoStop macro


## -description



The <b>capGrabFrameNoStop</b> macro fills the frame buffer with a single uncompressed frame from the capture device and displays it. Unlike with the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-capgrabframe">capGrabFrame</a> macro, the state of overlay or preview is not altered by this message. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-grab-frame-nostop">WM_CAP_GRAB_FRAME_NOSTOP</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


## -remarks



For information about installing callback functions, see the <b>capSetCallbackOnError</b> and <b>capSetCallbackOnFrame</b> macros.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
 

 

