---
UID: NF:vfw.capCaptureAbort
title: capCaptureAbort macro (vfw.h)
description: The capCaptureAbort macro stops the capture operation. You can use this macro or explictly send the WM_CAP_ABORT message.
helpviewer_keywords: ["_win32_capCaptureAbort","capCaptureAbort","capCaptureAbort macro [Windows Multimedia]","multimedia.capcaptureabort","vfw/capCaptureAbort"]
old-location: multimedia\capcaptureabort.htm
tech.root: Multimedia
ms.assetid: a1c17695-ee91-4f76-a2be-a6e512903c8f
ms.date: 12/05/2018
ms.keywords: _win32_capCaptureAbort, capCaptureAbort, capCaptureAbort macro [Windows Multimedia], multimedia.capcaptureabort, vfw/capCaptureAbort
f1_keywords:
- vfw/capCaptureAbort
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
- capCaptureAbort
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capCaptureAbort macro


## -description



The <b>capCaptureAbort</b> macro stops the capture operation. You can use this macro or explictly send the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-abort">WM_CAP_ABORT</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


## -remarks



The capture operation must yield to use this macro.

In the case of step capture, the image data collected up to the point of the <b>capCaptureAbort</b> macro will be retained in the capture file, but audio will not be captured.

Use the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-capcapturestop">capCaptureStop</a> macro to halt step capture at the current position, and then capture audio.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-capcapturestop">capCaptureStop</a>
 

 

