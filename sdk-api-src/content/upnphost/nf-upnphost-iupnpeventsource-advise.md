---
UID: NF:upnphost.IUPnPEventSource.Advise
title: IUPnPEventSource::Advise
author: windows-sdk-content
description: The Advise method is invoked by the device host to begin receiving events from the hosted service.
old-location: upnp\iupnpeventsource_advise.htm
old-project: upnp
ms.assetid: ec68f4ff-7549-4d48-b347-0320bc55329c
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: Advise, Advise method [UPnP APIs], Advise method [UPnP APIs],IUPnPEventSource interface, IUPnPEventSource interface [UPnP APIs],Advise method, IUPnPEventSource.Advise, IUPnPEventSource::Advise, _upnp_iupnpeventsource_advise, upnp.iupnpeventsource_advise, upnphost/IUPnPEventSource::Advise
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnphost.dll
api_name:
 - IUPnPEventSource.Advise
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnphost.dll
req.irql: 
req.product: Windows UI
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
 

 

