---
UID: NF:vfw.capGrabFrameNoStop
title: capGrabFrameNoStop macro (vfw.h)
author: windows-sdk-content
description: The capGrabFrameNoStop macro fills the frame buffer with a single uncompressed frame from the capture device and displays it.
old-location: multimedia\capgrabframenostop.htm
tech.root: Multimedia
ms.assetid: 0782d69f-6c4f-44f5-abd4-2b833be2f487
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_win32_capGrabFrameNoStop, capGrabFrameNoStop, capGrabFrameNoStop macro [Windows Multimedia], multimedia.capgrabframenostop, vfw/capGrabFrameNoStop"
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
 - capGrabFrameNoStop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capGrabFrameNoStop macro


## -description



The <b>capGrabFrameNoStop</b> macro fills the frame buffer with a single uncompressed frame from the capture device and displays it. Unlike with the <a href="https://msdn.microsoft.com/bd306414-74a9-4683-ad63-797a37152e8f">capGrabFrame</a> macro, the state of overlay or preview is not altered by this message. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/5f6e3ce7-3595-456e-82c8-eeb162ace81a">WM_CAP_GRAB_FRAME_NOSTOP</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


## -remarks



For information about installing callback functions, see the <b>capSetCallbackOnError</b> and <b>capSetCallbackOnFrame</b> macros.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

