---
UID: NF:vfw.capCaptureStop
title: capCaptureStop macro
author: windows-sdk-content
description: The capCaptureStop macro stops the capture operation. You can use this macro or explicitly send the WM_CAP_STOP message.
old-location: multimedia\capcapturestop.htm
tech.root: Multimedia
ms.assetid: 79b33f36-1bf9-41f2-827f-d0cfa276113e
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "_win32_capCaptureStop, capCaptureStop, capCaptureStop macro [Windows Multimedia], multimedia.capcapturestop, vfw/capCaptureStop"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
 - capCaptureStop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capCaptureStop macro


## -description



The <b>capCaptureStop</b> macro stops the capture operation. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/0fea82f5-f381-485a-82ae-b081b3a5e402">WM_CAP_STOP</a> message.



In step frame capture, the image data that was collected before this message was sent is retained in the capture file. An equivalent duration of audio data is also retained in the capture file if audio capture was enabled.


## -parameters




### -param hwnd

Handle to a capture window. 


## -remarks



The capture operation must yield to use this message. Use the <a href="https://msdn.microsoft.com/a1c17695-ee91-4f76-a2be-a6e512903c8f">capCaptureAbort</a> macro to abandon the current capture operation.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

