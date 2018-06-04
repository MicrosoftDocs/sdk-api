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

# IMediaEventEx::SetNotifyWindow


## -description



The <code>SetNotifyWindow</code> method registers a window to process event notifications.




## -parameters




### -param hwnd [in]

Handle to the window, or <b>NULL</b> to stop receiving event messages.


### -param lMsg [in]

Window message to be passed as the notification.


### -param lInstanceData [in]

Value to be passed as the <i>lParam</i> parameter for the <i>lMsg</i> message.


## -returns



Returns S_OK if successful or E_INVALIDARG if the <i>hwnd</i> parameter is not a valid handle to a window.




## -remarks



This method designates a window that will process event notifications. Whenever the Filter Graph Manager puts an event in the event queue, it will also post a message to the designated window. The <i>hwnd</i> parameter specifies the window, and the <i>lMsg</i> parameter specifies the message. The application should define a private window message for this purpose. The message's <i>lParam</i> parameter is set to the value of <b>lInstanceData</b>, and the <i>wParam</i> parameter is set to zero.

When the window receives the message, it should call the <a href="https://msdn.microsoft.com/d7cbbf6d-c741-416f-b8dd-d9ca012d309a">IMediaEvent::GetEvent</a> method to retrieve the event. Events are asynchronous, so the queue might contain several events (or none). Call <b>GetEvent</b> repeatedly, until it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9d367b0a-c7ec-49d4-a41e-045ac81d2c51">IMediaEventEx Interface</a>
 

 

