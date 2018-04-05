---
UID: NF:vfw.capCaptureAbort
title: capCaptureAbort macro
author: windows-driver-content
description: The capCaptureAbort macro stops the capture operation. You can use this macro or explictly send the WM_CAP_ABORT message.
old-location: multimedia\capcaptureabort.htm
old-project: Multimedia
ms.assetid: a1c17695-ee91-4f76-a2be-a6e512903c8f
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "_win32_capCaptureAbort, capCaptureAbort, capCaptureAbort macro [Windows Multimedia], multimedia.capcaptureabort, vfw/capCaptureAbort"
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vfw.h
api_name:
-	capCaptureAbort
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# capCaptureAbort macro


## -description



The <b>capCaptureAbort</b> macro stops the capture operation. You can use this macro or explictly send the <a href="https://msdn.microsoft.com/a0479d73-8422-4833-9e8a-c262ec386f58">WM_CAP_ABORT</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


## -remarks



The capture operation must yield to use this macro.

In the case of step capture, the image data collected up to the point of the <b>capCaptureAbort</b> macro will be retained in the capture file, but audio will not be captured.

Use the <a href="https://msdn.microsoft.com/79b33f36-1bf9-41f2-827f-d0cfa276113e">capCaptureStop</a> macro to halt step capture at the current position, and then capture audio.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>



<a href="https://msdn.microsoft.com/79b33f36-1bf9-41f2-827f-d0cfa276113e">capCaptureStop</a>
 

 

