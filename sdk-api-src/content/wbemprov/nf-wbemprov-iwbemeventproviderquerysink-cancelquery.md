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

# IWbemEventProviderQuerySink::CancelQuery


## -description


Call the 
<b>IWbemEventProviderQuerySink::CancelQuery</b> method whenever a logical event consumer cancels a relevant event query filter with Windows Management. The 
<b>CancelQuery</b> method determines how an event provider responds to a relevant canceled event query filter. Whenever WMI retrieves a cancellation notice for an event query filter from a consumer, WMI calls 
<b>CancelQuery</b> to echo the cancellation to the responsible event provider. The event provider can examine the identifier of the query to determine which query is being canceled. The provider then modifies which events are being sent out based on the cancellation.


## -parameters




### -param dwId [in]

Identifier of the query which was canceled. This identifier was originally delivered to the provider by the 
<a href="https://msdn.microsoft.com/82f76b19-2035-4567-b619-31ce8a35e422">NewQuery</a> method of this interface.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.




## -remarks



Whenever a consumer registers a new event query filter, Windows Management calls the 
<a href="https://msdn.microsoft.com/82f76b19-2035-4567-b619-31ce8a35e422">IWbemEventProviderQuerySink::NewQuery</a> method with the query identifier. Later, when that query is unregistered, this method is called indicating which query is no longer outstanding.

Providers use this method to help optimize the generation of events internally.




## -see-also




<a href="https://msdn.microsoft.com/76a29d81-33c2-489f-a71d-2e85ba2617bf">IWbemEventProviderQuerySink</a>



<a href="https://msdn.microsoft.com/82f76b19-2035-4567-b619-31ce8a35e422">IWbemEventProviderQuerySink::NewQuery</a>
 

 

