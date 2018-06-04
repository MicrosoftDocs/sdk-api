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

# IUPnPEventSource::Advise


## -description


The 
<b>Advise</b> method is invoked by the device host to begin receiving events from the hosted service. The device host passes a pointer to its <a href="_com_iunknown">IUnknown</a> interface. The hosted service must query this <b>IUnknown</b> interface for the 
<a href="https://msdn.microsoft.com/431423c9-2873-422d-a28c-c4ef23109114">IUPnPEventSink</a> interface the service must use to send event notifications.


## -parameters




### -param pesSubscriber






#### - punkSubscriber [in]

Pointer to the device host's 
<a href="https://msdn.microsoft.com/431423c9-2873-422d-a28c-c4ef23109114">IUPnPEventSink</a> interface.


## -returns



When implementing this method, return S_OK if the method succeeds. Otherwise, return one of the COM error codes defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/f20dfcaa-b8fe-43c8-b353-067dad4cf2b4">IUPnPEventSource</a>



<a href="https://msdn.microsoft.com/6ae9c53f-eb82-4396-ba85-c95e252911c8">IUPnPEventSource::Unadvise</a>
 

 

