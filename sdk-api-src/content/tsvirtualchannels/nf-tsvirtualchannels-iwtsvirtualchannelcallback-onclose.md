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

# IWTSVirtualChannelCallback::OnClose


## -description


Notifies the user that the channel has been closed. There are three ways for the channel to 
    be closed:
<ul>
<li>The user has called the 
     <a href="https://msdn.microsoft.com/b900789d-c7da-4974-8c46-72ea8ffd6892">IWTSVirtualChannel::Close</a> method.</li>
<li>The Remote Desktop Connection (RDC) client has disconnected from the Remote Desktop Session Host (RD Session Host) 
     server.</li>
<li>The server has called the 
     <a href="https://msdn.microsoft.com/d82cb1cd-a9bd-45e8-8a86-2c7dd860b987">WTSVirtualChannel::Close</a> method on the 
     channel.</li>
</ul>Regardless of how the channel has been closed, there is no need to call 
    <a href="https://msdn.microsoft.com/b900789d-c7da-4974-8c46-72ea8ffd6892">IWTSVirtualChannel::Close()</a> when this call 
    is received. If such a call is made, it is possible that if the plug-in is running out of process, that a call to 
    <b>IWTSVirtualChannel::Close()</b> may cause a 
    deadlock. A deadlock may occur because the caller of 
    <b>OnClose()</b> holds a channel list 
    lock, and the <b>Close()</b> method will try to 
    acquire the same lock on a different thread.


## -parameters






## -returns



Returns <b>S_OK</b> on success. Results in no action if the call fails.




## -see-also




<a href="https://msdn.microsoft.com/d90c6f80-ed4c-4b99-af85-d2c5816ade85">IWTSVirtualChannelCallback</a>
 

 

