---
UID: NF:vfw.capSetCallbackOnFrame
title: capSetCallbackOnFrame macro (vfw.h)
description: The capSetCallbackOnFrame macro sets a preview callback function in the application. AVICap calls this procedure when the capture window captures preview frames. You can use this macro or explicitly call the WM_CAP_SET_CALLBACK_FRAME message.
helpviewer_keywords: ["_win32_capSetCallbackOnFrame","capSetCallbackOnFrame","capSetCallbackOnFrame macro [Windows Multimedia]","multimedia.capsetcallbackonframe","vfw/capSetCallbackOnFrame"]
old-location: multimedia\capsetcallbackonframe.htm
tech.root: Multimedia
ms.assetid: 7e9e33cb-9213-4111-a1de-700493949f2d
ms.date: 12/05/2018
ms.keywords: _win32_capSetCallbackOnFrame, capSetCallbackOnFrame, capSetCallbackOnFrame macro [Windows Multimedia], multimedia.capsetcallbackonframe, vfw/capSetCallbackOnFrame
f1_keywords:
- vfw/capSetCallbackOnFrame
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
- capSetCallbackOnFrame
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capSetCallbackOnFrame macro


## -description



The <b>capSetCallbackOnFrame</b> macro sets a preview callback function in the application. AVICap calls this procedure when the capture window captures preview frames. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-set-callback-frame">WM_CAP_SET_CALLBACK_FRAME</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param fpProc

Pointer to the preview callback function, of type <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nc-vfw-capvideocallback">capVideoStreamCallback</a>. Specify <b>NULL</b> for this parameter to disable a previously installed callback function. 


## -remarks



The capture window calls the callback function before displaying preview frames. This allows an application to modify the frame if desired. This callback function is not used during streaming video capture.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/creating-a-frame-callback-function">Creating a Frame Callback Function</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
 

 

