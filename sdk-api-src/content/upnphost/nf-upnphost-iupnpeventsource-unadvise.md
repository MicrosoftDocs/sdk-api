---
UID: NF:upnphost.IUPnPEventSource.Unadvise
title: IUPnPEventSource::Unadvise
author: windows-sdk-content
description: The Unadvise method is invoked by the device host to stop receiving events. The device host passes in the same pointer that it did when it invoked the IUPnPEventSource::Advise method.
old-location: upnp\iupnpeventsource_unadvise.htm
old-project: UPnP
ms.assetid: 6ae9c53f-eb82-4396-ba85-c95e252911c8
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: IUPnPEventSource interface [UPnP APIs],Unadvise method, IUPnPEventSource.Unadvise, IUPnPEventSource::Unadvise, Unadvise, Unadvise method [UPnP APIs], Unadvise method [UPnP APIs],IUPnPEventSource interface, _upnp_iupnpeventsource_unadvise, upnp.iupnpeventsource_unadvise, upnphost/IUPnPEventSource::Unadvise
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: upnphost.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Upnphost.dll
api_name:
-	IUPnPEventSource.Unadvise
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnphost.dll
req.irql: 
req.product: Windows UI
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
 

 

