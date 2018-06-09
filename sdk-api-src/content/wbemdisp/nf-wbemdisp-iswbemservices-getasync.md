---
UID: NF:wbemdisp.ISWbemServices.GetAsync
title: ISWbemServices::GetAsync
author: windows-sdk-content
description: Retrieves an object, that is a class definition or an instance, based on the object path.
old-location: wmi\swbemservices_getasync.htm
old-project: WmiSdk
ms.assetid: 8da46851-52b8-4b5a-8c9d-1d492f57f4b6
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: GetAsync, GetAsync method [Windows Management Instrumentation], GetAsync method [Windows Management Instrumentation],ISWbemServices interface, GetAsync method [Windows Management Instrumentation],SWbemServices object, ISWbemServices interface [Windows Management Instrumentation],GetAsync method, ISWbemServices.GetAsync, ISWbemServices::GetAsync, SWbemServices object [Windows Management Instrumentation],GetAsync method, SWbemServices.GetAsync, _hmm_swbemservices.getasync, wbemFlagDontSendStatus, wbemFlagSendStatus, wbemFlagUseAmendedQualifiers, wmi.swbemservices_getasync
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
 - SWbemServices.GetAsync
 - ISWbemServices.GetAsync
 - ISWbemServices.GetAsync
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemServices::GetAsync


## -description


The 
<b>GetAsync</b> method of the 
<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object retrieves an object, that is a class definition or an instance, based on the object path.

This method retrieves only objects from the namespace that is associated with the current 
<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object.

This method is called in the asynchronous mode. For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param objWbemSink

Required. Object sink that gets objects asynchronously. Create a <a href="https://msdn.microsoft.com/a90777ef-fa26-4bfb-b196-c083a0c92a29">SWbemSink</a> object to receive the objects.


### -param strObjectPath [optional]

Path of the object that you want to retrieve. If this value is empty, the empty object that is returned can become a new class.  For more information, see <a href="https://msdn.microsoft.com/7a390541-609d-4b97-b91c-1a41d21ec17d">Describing the Location of a WMI Object</a>.


### -param iFlags [optional]

Integer that determines the behavior of the call. This parameter can accept the following values.



#### wbemFlagSendStatus (128 (0x80))

Causes asynchronous calls to send status updates to the 
<a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">OnProgress</a> event handler for the object sink.



#### wbemFlagDontSendStatus (0 (0x0))

Prevents asynchronous calls from sending status updates to the 
<a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">OnProgress</a> event handler for the object sink.



#### wbemFlagUseAmendedQualifiers (131072 (0x20000))

Causes WMI to return class amendment data with the base class definition. 
For more information, see <a href="https://msdn.microsoft.com/01e1cee5-d882-45b6-ac93-68533c2c6c9d">Localizing WMI Class Information</a>.


### -param objWbemNamedValueSet




### -param objWbemAsyncContext [optional]

An 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object that returns to the object sink to identify the source of the original asynchronous call. Use this parameter if you are making multiple asynchronous calls using the same object sink. To use this parameter, create an <b>SWbemNamedValueSet</b> object and use the <a href="https://msdn.microsoft.com/471b23f5-6c53-40e2-a2a9-0798044c9dfb">SWbemNamedValueSet.Add</a> method to add a value that identifies the asynchronous call you are making. This <b>SWbemNamedValueSet</b> object is returned to the object sink and the source of the call can be extracted using the <a href="https://msdn.microsoft.com/ccebe65e-6032-43d5-9004-2247c3b96d6d">SWbemNamedValueSet.Item</a> method. For more information, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


#### - objwbemNamedValueSet [optional]

Typically, this value is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that is servicing the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


## -returns



This method does not return a value. If successful, the sink receives an 
<a href="https://msdn.microsoft.com/14110ee7-a808-4786-b695-2ce54189d826">OnObjectReady</a> event when the object is available.




## -remarks



This call returns immediately.  The requested object and status are returned to the caller through a callback delivered to the sink that is specified in <i>objWbemSink</i>. To process the object when it returns, create an <i>objWbemSink</i>.<a href="https://msdn.microsoft.com/14110ee7-a808-4786-b695-2ce54189d826">OnObjectReady</a>, or an <i>objWbemSink</i>.<a href="https://msdn.microsoft.com/2723185d-5b8b-4cc7-ada3-51c3275272a9">OnCompleted</a> event subroutine.

An asynchronous callback allows a non-authenticated user to provide data to the sink. This poses security risks to your scripts and applications. To eliminate the risks, use semisynchronous or synchronous communication.
For more information, see <a href="https://msdn.microsoft.com/2b839ea9-e1e6-4123-a98a-04ebee907b3b">Setting Security on an Asynchronous Call</a>.




## -see-also




<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>



<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a>
 

 

