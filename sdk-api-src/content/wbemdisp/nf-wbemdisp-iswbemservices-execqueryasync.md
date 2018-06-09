---
UID: NF:wbemdisp.ISWbemServices.ExecQueryAsync
title: ISWbemServices::ExecQueryAsync
author: windows-sdk-content
description: Executes a query to retrieve objects.
old-location: wmi\swbemservices_execqueryasync.htm
old-project: WmiSdk
ms.assetid: 50c7f62b-dd83-4117-b10e-acee1690ce8c
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ExecQueryAsync, ExecQueryAsync method [Windows Management Instrumentation], ExecQueryAsync method [Windows Management Instrumentation],ISWbemServices interface, ExecQueryAsync method [Windows Management Instrumentation],SWbemServices object, ISWbemServices interface [Windows Management Instrumentation],ExecQueryAsync method, ISWbemServices.ExecQueryAsync, ISWbemServices::ExecQueryAsync, SWbemServices object [Windows Management Instrumentation],ExecQueryAsync method, SWbemServices.ExecQueryAsync, _hmm_swbemservices.execqueryasync, wbemFlagDontSendStatus, wbemFlagSendStatus, wbemFlagUseAmendedQualifiers, wbemQueryFlagPrototype, wmi.swbemservices_execqueryasync
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
 - SWbemServices.ExecQueryAsync
 - ISWbemServices.ExecQueryAsync
 - ISWbemServices.ExecQueryAsync
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemServices::ExecQueryAsync


## -description


The 
<b>ExecQueryAsync</b> method of the 
<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object executes a query to retrieve objects. The call to this method returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in <i>objWbemSink</i>. To handle each returned object, create an <i>objWbemSink</i>.<a href="https://msdn.microsoft.com/14110ee7-a808-4786-b695-2ce54189d826">OnObjectReady</a> event subroutine.

The method is called in the asynchronous mode. For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param objWbemSink [optional]

Object sink that executes the query asynchronously. Create an <a href="https://msdn.microsoft.com/a90777ef-fa26-4bfb-b196-c083a0c92a29">SWbemSink</a> object to receive the objects.


### -param strQuery

Required. String that contains the text of the query. This parameter cannot be blank. For more information on building WMI query strings, see <a href="https://msdn.microsoft.com/7e04ba37-c0e0-4304-b162-8b911f233f38">Querying with WQL</a> and the <a href="https://msdn.microsoft.com/72a7ec04-9af3-41ae-9189-6e1d46803fa9">WQL</a> reference.


### -param strQueryLanguage [optional]

String that contains the query language to be used. If specified, the value must be "WQL".


### -param lFlags




### -param objWbemNamedValueSet




### -param objWbemAsyncContext [optional]

An 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object that returns to the object sink to identify the source of the original asynchronous call. Use this parameter to make multiple asynchronous calls using the same object sink. To use this parameter, create an <b>SWbemNamedValueSet</b> object, and use the <a href="https://msdn.microsoft.com/471b23f5-6c53-40e2-a2a9-0798044c9dfb">SWbemNamedValueSet.Add</a> method to add a value that identifies the asynchronous call you are making. This <b>SWbemNamedValueSet</b> object is returned to the object sink and the source of the call can be extracted using the <a href="https://msdn.microsoft.com/ccebe65e-6032-43d5-9004-2247c3b96d6d">SWbemNamedValueSet.Item</a> method. For more information, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


#### - iFlags [optional]

Integer that determines the behavior of the query. This parameter can accept the following values.



#### wbemFlagSendStatus (128 (0x80))

Causes asynchronous calls to send status updates to the 
<a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">OnProgress</a> event handler for the object sink.



#### wbemFlagDontSendStatus (0 (0x0))

Prevents asynchronous calls from sending status updates to the 
<a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">OnProgress</a> event handler for the object sink.



#### wbemQueryFlagPrototype (2 (0x2))

Used for a prototype. It stops the query from happening and instead, returns an object that looks like a typical result object.



#### wbemFlagUseAmendedQualifiers (131072 (0x20000))

Causes WMI to return class amendment data  with the base class definition. 
For more information, see <a href="https://msdn.microsoft.com/01e1cee5-d882-45b6-ac93-68533c2c6c9d">Localizing WMI Class Information</a>.


#### - objwbemNamedValueSet [optional]

Typically, this is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that services the request. A provider that supports or requires context information must document the recognized value names, data type of the value, allowed values, and semantics.


## -returns



This method has no return values. If successful, the sink receives an 
<a href="https://msdn.microsoft.com/14110ee7-a808-4786-b695-2ce54189d826">OnObjectReady</a> event per instance. After the last instance, the object sink receives an 
<a href="https://msdn.microsoft.com/2723185d-5b8b-4cc7-ada3-51c3275272a9">OnCompleted</a> event.




## -remarks



This call returns immediately.  The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in <i>objWbemSink</i>. To process each object when it returns, create an <i>objWbemSink</i>.<a href="https://msdn.microsoft.com/14110ee7-a808-4786-b695-2ce54189d826">OnObjectReady</a> event subroutine. After all the objects are returned, perform the final processing in your implementation of the  <i>objWbemSink</i>.<a href="https://msdn.microsoft.com/2723185d-5b8b-4cc7-ada3-51c3275272a9">OnCompleted</a> event.

An asynchronous callback allows a non-authenticated user to provide data to the sink. This poses security risks to your scripts and applications. To eliminate the risks, see <a href="https://msdn.microsoft.com/2b839ea9-e1e6-4123-a98a-04ebee907b3b">Setting Security on an Asynchronous Call</a>


The 
<b>ExecQueryAsync</b> method returns an empty result set when there are no objects to match the criteria in the query. This method returns key properties whether or not the <a href="https://msdn.microsoft.com/library/windows/hardware/dn895751">Key</a> property is requested in the <i>strQuery</i> parameter.

There are limits to the number of <b>AND</b> and <b>OR</b> keywords that can be used in WQL queries.  Large numbers of WQL keywords used in a complex query can cause WMI to return the WBEM_E_QUOTA_VIOLATION error code as an <b>HRESULT</b> value.  The limit of WQL keywords depends on how complex the query is.




## -see-also




<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>



<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a>



<a href="https://msdn.microsoft.com/3071aeb2-adab-47aa-a10c-9796766bb630">SWbemServices.Get</a>
 

 

