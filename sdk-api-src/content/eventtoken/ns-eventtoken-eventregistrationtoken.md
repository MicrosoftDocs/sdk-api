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

# EventRegistrationToken structure


## -description


Identifies an event handler that has been registered with an event source.


## -struct-fields




### -field value

Type: <b>INT64</b>

An identifying value that is provided by an event source. 


## -remarks



Use an <b>EventRegistrationToken</b> to  unsubscribe from a Windows Runtime event source.

You acquire an <b>EventRegistrationToken</b> when you subscribe to an event. 




## -see-also




<a href="https://msdn.microsoft.com/E9F74A4B-8678-4C40-8D6D-4779D7E5869E">IEventHandler<T></a>



<a href="https://msdn.microsoft.com/94B238FB-24F0-43FC-9F84-E30FE9081B50">ITypedEventHandler<TSender, TArgs></a>
 

 

