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

# IMediaEventSink::Notify


## -description



The <code>Notify</code> method notifies the Filter Graph Manager of an event.




## -parameters




### -param EventCode [in]

Identifier of the event.


### -param EventParam1 [in]

First event parameter.


### -param EventParam2 [in]

Second event parameter.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



The event is queued but not delivered to the application on this thread. For a list of notification codes and event parameter values, see <a href="https://msdn.microsoft.com/339ffcd9-7724-4c92-b241-afbed81d9380">Event Notification Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/50aa04b4-9a04-4d0d-a558-42595a69aef7">IMediaEventSink Interface</a>
 

 

