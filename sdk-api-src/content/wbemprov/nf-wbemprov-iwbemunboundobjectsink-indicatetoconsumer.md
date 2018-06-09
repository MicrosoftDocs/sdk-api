---
UID: NF:wbemprov.IWbemUnboundObjectSink.IndicateToConsumer
title: IWbemUnboundObjectSink::IndicateToConsumer
author: windows-sdk-content
description: Called by WMI to actually deliver events to a consumer.
old-location: wmi\iwbemunboundobjectsink_indicatetoconsumer.htm
old-project: WmiSdk
ms.assetid: 70fe9976-cfa9-442d-93a4-12293e80d1fa
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: IWbemUnboundObjectSink interface [Windows Management Instrumentation],IndicateToConsumer method, IWbemUnboundObjectSink.IndicateToConsumer, IWbemUnboundObjectSink::IndicateToConsumer, IndicateToConsumer, IndicateToConsumer method [Windows Management Instrumentation], IndicateToConsumer method [Windows Management Instrumentation],IWbemUnboundObjectSink interface, _hmm_iwbemunboundobjectsink_indicatetoconsumer, wbemprov/IWbemUnboundObjectSink::IndicateToConsumer, wmi.iwbemunboundobjectsink_indicatetoconsumer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemprov.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fastprox.dll
api_name:
 - IWbemUnboundObjectSink.IndicateToConsumer
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

