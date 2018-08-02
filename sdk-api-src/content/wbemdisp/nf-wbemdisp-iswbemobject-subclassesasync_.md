---
UID: NF:wbemdisp.ISWbemObject.SubclassesAsync_
title: ISWbemObject::SubclassesAsync_
author: windows-sdk-content
description: The SubclassesAsync_ method of SWbemObject asynchronously supplies the subclasses of the current object, which must be a class.
old-location: wmi\swbemobject_subclassesasync_.htm
old-project: WmiSdk
ms.assetid: 14d4a609-3aa4-49bd-bea4-6a71bc24d9dd
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISWbemObject interface [Windows Management Instrumentation],SubclassesAsync_ method, ISWbemObject.SubclassesAsync_, ISWbemObject::SubclassesAsync_, SWbemObject object [Windows Management Instrumentation],SubclassesAsync_ method, SWbemObject.SubclassesAsync_, SubclassesAsync_, SubclassesAsync_ method [Windows Management Instrumentation], SubclassesAsync_ method [Windows Management Instrumentation],ISWbemObject interface, SubclassesAsync_ method [Windows Management Instrumentation],SWbemObject object, _hmm_swbemobject.subclassesasync_, wbemFlagDontSendStatus, wbemFlagSendStatus, wbemFlagUseAmendedQualifiers, wbemQueryFlagDeep, wbemQueryFlagShallow, wmi.swbemobject_subclassesasync_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
req.include-header: 
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
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemObject.SubclassesAsync_
 - ISWbemObject.SubclassesAsync_
 - ISWbemObject.SubclassesAsync_
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObject::SubclassesAsync_


## -description


The 
<b>SubclassesAsync_</b> method of <a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> asynchronously supplies the subclasses of the current object, which must be a class.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param objWbemSink [in]

Required. Object sink that receives the objects asynchronously.


### -param iFlags [in, optional]

Determines how detailed the call enumerates. This parameter can accept the following values.



#### wbemQueryFlagDeep (0 (0x0))

Forces recursive enumeration into all subclasses derived from the specified parent class. The parent class itself is not returned in the enumeration.



#### wbemQueryFlagShallow (1 (0x1))

Default for this parameter. It forces the enumeration to include only immediate subclasses of the specified parent class.



#### wbemFlagSendStatus (128 (0x80))

Causes asynchronous calls to send status updates to the 
<a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">SWbemSink.OnProgress</a> event handler for the object sink.



#### wbemFlagDontSendStatus (0 (0x0))

Prevents asynchronous calls from sending status updates to the 
<a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">OnProgress</a> event handler for the object sink.



#### wbemFlagUseAmendedQualifiers (131072 (0x20000))

Causes WMI to return class amendment data with the base class definition. 
For more information about amended qualifiers, see <a href="https://msdn.microsoft.com/01e1cee5-d882-45b6-ac93-68533c2c6c9d">Localizing WMI Class Information</a>.


### -param objWbemNamedValueSet [in, optional]

Typically, this is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that is servicing the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


### -param objWbemAsyncContext [in, optional]

This is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object that returns to the object sink to identify the source of the original asynchronous call. Use this parameter when you make multiple asynchronous calls using the same object sink. To use this parameter, create an <b>SWbemNamedValueSet</b> object, and use the <a href="https://msdn.microsoft.com/471b23f5-6c53-40e2-a2a9-0798044c9dfb">SWbemNamedValueSet.Add</a> method to add a value that identifies the asynchronous call you are making. This <b>SWbemNamedValueSet</b> object is returned to the object sink, and the source of the call can be extracted using the <a href="https://msdn.microsoft.com/ccebe65e-6032-43d5-9004-2247c3b96d6d">SWbemNamedValueSet.Item</a> method. For more information, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


## -returns



This method does not return a value. If successful, the sink receives an 
<a href="https://msdn.microsoft.com/14110ee7-a808-4786-b695-2ce54189d826">OnObjectReady</a> event for each instance. After the last instance, the object sink  receives an 
<a href="https://msdn.microsoft.com/2723185d-5b8b-4cc7-ada3-51c3275272a9">OnCompleted</a> event.




## -remarks



This call returns immediately.  The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in <i>objWbemSink</i>. To process each object when it arrives, create an <i>objWbemSink</i>.<a href="https://msdn.microsoft.com/14110ee7-a808-4786-b695-2ce54189d826">OnObjectReady</a> event subroutine. After all the objects are returned, you can perform final processing in your implementation of the  <i>objWbemSink</i>.<a href="https://msdn.microsoft.com/2723185d-5b8b-4cc7-ada3-51c3275272a9">OnCompleted</a> event.

An asynchronous callback allows a non-authenticated user to provide data to the sink. This poses security risks to your scripts and applications. To eliminate the risks, use either semisynchronous communication or synchronous communication.
For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

It is  recommended that scripts verify the source of the call by using an <i>objWbemAsyncContext</i> parameter.

It is not an error for the returned collection to have zero elements if there are no subclasses of the current object. The 
<b>SubclassesAsync_</b> method only works for class objects.




## -see-also




<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>



<a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a>



<a href="https://msdn.microsoft.com/6a12c8eb-3ef9-4292-810c-6954294fc8c7">SWbemRefreshableItem</a>
 

 

