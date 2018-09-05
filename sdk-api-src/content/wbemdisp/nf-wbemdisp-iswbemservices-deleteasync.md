---
UID: NF:wbemdisp.ISWbemServices.DeleteAsync
title: ISWbemServices::DeleteAsync
author: windows-sdk-content
description: Deletes the class or instance specified in the object path.
old-location: wmi\swbemservices_deleteasync.htm
old-project: WmiSdk
ms.assetid: f5ed170e-d002-4dd9-b8b6-b764a7a41a27
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: DeleteAsync, DeleteAsync method [Windows Management Instrumentation], DeleteAsync method [Windows Management Instrumentation],ISWbemServices interface, DeleteAsync method [Windows Management Instrumentation],SWbemServices object, ISWbemServices interface [Windows Management Instrumentation],DeleteAsync method, ISWbemServices.DeleteAsync, ISWbemServices::DeleteAsync, SWbemServices object [Windows Management Instrumentation],DeleteAsync method, SWbemServices.DeleteAsync, _hmm_swbemservices.deleteasync, wbemFlagDontSendStatus, wbemFlagSendStatus, wmi.swbemservices_deleteasync
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
req.include-header: 
req.redist: 
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
 - SWbemServices.DeleteAsync
 - ISWbemServices.DeleteAsync
 - ISWbemServices.DeleteAsync
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemServices::DeleteAsync


## -description


The 
<b>DeleteAsync</b> method of the 
<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object deletes the class or instance specified in the object path. The call to <b>DeleteAsync </b>returns immediately and the results and status are returned to the caller through events delivered to the sink that is specified in <i>objWbemSink</i>. For more information about creating a sink, see 
<a href="https://msdn.microsoft.com/347808a7-0f7b-4687-93f4-bea55c96795a">Receiving a WMI Event</a>. You can only delete objects in the namespace to which you are connected.

If a dynamic provider supplies the class or instance, sometimes it is  not possible to delete this object unless the provider supports class or instance deletion.

The method is called in the asynchronous mode. For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param objWbemSink




### -param strObjectPath

Required. String that contains the object path to the object that you want to delete. For more information, see <a href="https://msdn.microsoft.com/7a390541-609d-4b97-b91c-1a41d21ec17d">Describing the Location of a WMI Object</a>.


### -param iFlags [optional]

Determines if status updates are returned. This parameter can accept the following values.



#### wbemFlagSendStatus (128 (0x80))

Causes asynchronous calls to send status updates to the 
<a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">OnProgress</a> event handler for the object sink.



#### wbemFlagDontSendStatus (0 (0x0))

Prevents asynchronous calls from sending status updates to the 
<a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">OnProgress</a> event handler for the object sink.


### -param objWbemNamedValueSet [optional]

Typically, this is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that is servicing the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


### -param objWbemAsyncContext [optional]

An 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object that returns to the object sink to identify the source of the original asynchronous call. Use this parameter if you are making multiple asynchronous calls using the same object sink. To use this parameter, create an <b>SWbemNamedValueSet</b> object and use the <a href="https://msdn.microsoft.com/471b23f5-6c53-40e2-a2a9-0798044c9dfb">SWbemNamedValueSet.Add</a> method to add a value that identifies the asynchronous call you are making. This <b>SWbemNamedValueSet</b> object is returned to the object sink and the source of the call can be extracted using the <a href="https://msdn.microsoft.com/ccebe65e-6032-43d5-9004-2247c3b96d6d">SWbemNamedValueSet.Item</a> method. For more information, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


#### - ObjWbemSink [optional]

Object sink that receives the results of the deletion. Create an <a href="https://msdn.microsoft.com/a90777ef-fa26-4bfb-b196-c083a0c92a29">SWbemSink</a> object to receive the objects.


## -returns



This method does not return a value. If the call is successful, the object sink  receives notification of the deletion.




## -remarks



This call returns immediately.  The status of the delete operation is returned to the caller through a callback delivered to the sink that is specified in <i>objWbemSink</i>. You can perform final processing in your implementation of the  <i>objWbemSink</i>.<a href="https://msdn.microsoft.com/2723185d-5b8b-4cc7-ada3-51c3275272a9">OnCompleted</a> event.

An asynchronous callback allows a non-authenticated user to provide data to the sink. This poses security risks to your scripts and applications. To eliminate the risks, see <a href="https://msdn.microsoft.com/2b839ea9-e1e6-4123-a98a-04ebee907b3b">Setting Security on an Asynchronous Call</a>.




## -see-also




<a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a>



<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a>
 

 

