---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

