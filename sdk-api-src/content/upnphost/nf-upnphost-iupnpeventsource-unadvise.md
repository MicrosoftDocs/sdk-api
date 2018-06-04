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

# IUPnPEventSource::Unadvise


## -description


The 
<b>Unadvise</b> method is invoked by the device host to stop receiving events. The device host passes in the same pointer that it did when it invoked the 
<a href="https://msdn.microsoft.com/ec68f4ff-7549-4d48-b347-0320bc55329c">IUPnPEventSource::Advise</a> method.

After this method is invoked, the hosted service releases the reference to the event sink that it held.


## -parameters




### -param pesSubscriber






#### - punkSubscriber [in]

Pointer to the device host's 
<a href="https://msdn.microsoft.com/431423c9-2873-422d-a28c-c4ef23109114">IUPnPEventSink</a> interface. This must be the same pointer that was passed when 
<a href="https://msdn.microsoft.com/ec68f4ff-7549-4d48-b347-0320bc55329c">IUPnPEventSource::Advise</a> was invoked.


## -returns



When implementing this method, return S_OK if the method succeeds. Otherwise, return one of the COM error codes defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/f20dfcaa-b8fe-43c8-b353-067dad4cf2b4">IUPnPEventSource</a>



<a href="https://msdn.microsoft.com/ec68f4ff-7549-4d48-b347-0320bc55329c">IUPnPEventSource::Advise</a>
 

 

