---
UID: NF:vfw.capSetCallbackOnWaveStream
title: capSetCallbackOnWaveStream macro (vfw.h)
author: windows-sdk-content
description: The capSetCallbackOnWaveStream macro sets a callback function in the application.
old-location: multimedia\capsetcallbackonwavestream.htm
tech.root: Multimedia
ms.assetid: 282386af-506b-4be6-bb75-aa3c62f9778a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_win32_capSetCallbackOnWaveStream, capSetCallbackOnWaveStream, capSetCallbackOnWaveStream macro [Windows Multimedia], multimedia.capsetcallbackonwavestream, vfw/capSetCallbackOnWaveStream"
ms.topic: macro
f1_keywords: 
 - "vfw/capSetCallbackOnWaveStream"
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
 - capSetCallbackOnWaveStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capSetCallbackOnWaveStream macro


## -description



The <b>capSetCallbackOnWaveStream</b> macro sets a callback function in the application. AVICap calls this procedure during streaming capture when a new audio buffer becomes available. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-set-callback-wavestream">WM_CAP_SET_CALLBACK_WAVESTREAM</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param fpProc

Pointer to the wave stream callback function, of type <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nc-vfw-capwavecallback">capWaveStreamCallback</a>. Specify <b>NULL</b> for this parameter to disable a previously installed wave stream callback function. 


## -remarks



The capture window calls the procedure before writing the audio buffer to disk. This allows applications to modify the audio buffer if desired.

If a wave stream callback function is used, it must be installed before starting the capture session and it must remain enabled for the duration of the session. It can be disabled after streaming capture ends.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
 

 

