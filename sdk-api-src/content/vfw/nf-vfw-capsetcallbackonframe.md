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

# capSetCallbackOnFrame macro


## -description



The <b>capSetCallbackOnFrame</b> macro sets a preview callback function in the application. AVICap calls this procedure when the capture window captures preview frames. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/3882e6f6-c48c-4e50-9697-cbdf5b9342a5">WM_CAP_SET_CALLBACK_FRAME</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param fpProc

Pointer to the preview callback function, of type <a href="https://msdn.microsoft.com/e21d7563-0ca8-4777-9fb0-de7c1c4ae618">capVideoStreamCallback</a>. Specify <b>NULL</b> for this parameter to disable a previously installed callback function. 


## -remarks



The capture window calls the callback function before displaying preview frames. This allows an application to modify the frame if desired. This callback function is not used during streaming video capture.




## -see-also




<a href="https://msdn.microsoft.com/37002ee0-9907-4aab-93cc-50fe9cd21cff">Creating a Frame Callback Function</a>



<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

