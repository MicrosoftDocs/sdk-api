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

# SENS_QOCINFO structure


## -description


The 
<b>SENS_QOCINFO</b> structure is used by the 
<a href="https://msdn.microsoft.com/3b067a6f-ba4c-4914-aa5b-e0fd7690e75c">ISensNetwork::ConnectionMade</a> method. This structure contains Quality of Connection information to the sink object in an application that subscribes to SENS.


## -struct-fields




### -field dwSize

This member contains the actual size of the structure that was filled in.


### -field dwFlags

Speed of connection. Flag bits indicate whether the connection is slow, medium, fast.


### -field dwOutSpeed

Speed of data sent to the destination in bits per second.


### -field dwInSpeed

Speed of data coming in from the destination in bits per second.


## -see-also




<a href="https://msdn.microsoft.com/f313588f-6257-4a0d-b95a-aabc0bc64b53">About System Event Notification Service</a>



<a href="_cos_ieventsubscription">IEventSubscription</a>



<a href="_cos_ieventsubscription_putpublisherproperty">IEventSubscription::PutPublisherProperty</a>



<a href="https://msdn.microsoft.com/3b067a6f-ba4c-4914-aa5b-e0fd7690e75c">ISensNetwork::ConnectionMade</a>
 

 

