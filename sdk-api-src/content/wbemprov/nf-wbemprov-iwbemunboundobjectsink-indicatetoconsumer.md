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

# IWbemUnboundObjectSink::IndicateToConsumer


## -description


The 
<b>IWbemUnboundObjectSink::IndicateToConsumer</b> method is called by WMI to actually deliver events to a consumer. From an implementation standpoint, 
<b>IndicateToConsumer</b> contains the code for processing events that the sink receives.


## -parameters




### -param pLogicalConsumer [in]

Pointer to the logical consumer object for which this set of objects is delivered.


### -param lNumObjects [in]

Number of objects delivered in the array that follows.


### -param apObjects [in]

Pointer to an array of 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> instances which represent the events delivered. Because each object in the array corresponds to a separate event, an implementation of 
<b>IndicateToConsumer</b> must treat each object separately.


## -returns



This method returns <b>WBEM_S_NO_ERROR</b> if successful. Otherwise, the implementation should return an appropriate error code.




## -remarks



WMI typically obtains the 
<a href="https://msdn.microsoft.com/a890aefe-e35e-4635-874d-953194f99a82">IWbemUnboundObjectSink</a> pointer for a particular logical consumer from a event consumer provider which implements the 
<a href="https://msdn.microsoft.com/793bbc22-4a8b-4ab3-8cfe-7d81f42a6b7f">IWbemEventConsumerProvider</a> interface. Then, Windows Management calls 
<b>IndicateToConsumer</b> to deliver the actual event objects.

Most implementations of 
<b>IndicateToConsumer</b> assume that the notification is asynchronous. To support synchronous notification, a sink must complete event processing in less than 20 milliseconds. Extremely fast event consumer providers that support synchronous notification must not hold the pointer to the 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> interface or increment the pointer reference count in 
<b>IndicateToConsumer</b>. If 
<b>IndicateToConsumer</b> requires the class object defined by 
<b>IWbemClassObject</b> beyond the lifetime of the 
<b>IndicateToConsumer</b> call, make a copy of the object. However, if there must be long-term access to the information pointed to by the 
<b>IWbemClassObject</b> pointer, it is recommended that the event consumer provider not support synchronous notification. Event consumer providers indicate the type of notification that they support when they complete their registration.




## -see-also




<a href="https://msdn.microsoft.com/793bbc22-4a8b-4ab3-8cfe-7d81f42a6b7f">IWbemEventConsumerProvider</a>



<a href="https://msdn.microsoft.com/a890aefe-e35e-4635-874d-953194f99a82">IWbemUnboundObjectSink</a>
 

 

