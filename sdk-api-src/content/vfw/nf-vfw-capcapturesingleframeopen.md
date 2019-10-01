---
UID: NF:vfw.capCaptureSingleFrameOpen
title: capCaptureSingleFrameOpen macro (vfw.h)
author: windows-sdk-content
description: The capCaptureSingleFrameOpen macro opens the capture file for single-frame capturing. Any previous information in the capture file is overwritten. You can use this macro or explicitly send the WM_CAP_SINGLE_FRAME_OPEN message.
old-location: multimedia\capcapturesingleframeopen.htm
tech.root: Multimedia
ms.assetid: 980ba1ef-d86a-47f6-9876-84b5a099d14d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_win32_capCaptureSingleFrameOpen, capCaptureSingleFrameOpen, capCaptureSingleFrameOpen macro [Windows Multimedia], multimedia.capcapturesingleframeopen, vfw/capCaptureSingleFrameOpen"
ms.topic: macro
f1_keywords: 
 - "vfw/capCaptureSingleFrameOpen"
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
 - capCaptureSingleFrameOpen
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capCaptureSingleFrameOpen macro


## -description



The <b>capCaptureSingleFrameOpen</b> macro opens the capture file for single-frame capturing. Any previous information in the capture file is overwritten. You can use this macro or explicitly send the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-single-frame-open">WM_CAP_SINGLE_FRAME_OPEN</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


## -remarks



For information about installing callback functions, see the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-capsetcallbackonerror">capSetCallbackOnError</a> and <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-capsetcallbackonframe">capSetCallbackOnFrame</a> macros.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
 

 

