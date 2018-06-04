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

# IWTSProtocolConnectionCallback::DisplayIOCtl


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnectionCallback::DisplayIOCtl</b> is no longer available for use as of Windows Server 2012.]

Requests that the Remote Desktop Services service send data to the display driver loaded in the session.


## -parameters




### -param DisplayIOCtl [in, optional]

A <a href="https://msdn.microsoft.com/1a052b7c-8c15-4921-8548-8fa461210e9a">WTS_DISPLAY_IOCTL</a> structure that contains data to be sent to the display driver loaded in the session.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



To avoid deadlocks when calling this method:

<ul>
<li>Create a separate thread on which to make the call. Do not make the call from inside of any protocol method that you are implementing.</li>
<li>Do not block on this method before replying to another call by the Remote Desktop Services service.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/ac8a2a66-fa1f-48bd-9502-def833e26f31">IWTSProtocolConnectionCallback</a>



<a href="https://msdn.microsoft.com/1a052b7c-8c15-4921-8548-8fa461210e9a">WTS_DISPLAY_IOCTL</a>
 

 

