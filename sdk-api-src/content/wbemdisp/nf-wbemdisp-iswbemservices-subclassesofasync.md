---
UID: NF:wbemdisp.ISWbemServices.SubclassesOfAsync
title: ISWbemServices::SubclassesOfAsync
author: windows-sdk-content
description: Returns a collection of subclasses for a specified class.
old-location: wmi\swbemservices_subclassesofasync.htm
old-project: WmiSdk
ms.assetid: a9d16ee9-992e-4ce5-9c03-0a2c9958588c
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ISWbemServices interface [Windows Management Instrumentation],SubclassesOfAsync method, ISWbemServices.SubclassesOfAsync, ISWbemServices::SubclassesOfAsync, SWbemServices object [Windows Management Instrumentation],SubclassesOfAsync method, SWbemServices.SubclassesOfAsync, SubclassesOfAsync, SubclassesOfAsync method [Windows Management Instrumentation], SubclassesOfAsync method [Windows Management Instrumentation],ISWbemServices interface, SubclassesOfAsync method [Windows Management Instrumentation],SWbemServices object, _hmm_swbemservices.subclassesofasync, asynchronous mode, wbemFlagDontSendStatus, wbemFlagSendStatus, wbemFlagUseAmendedQualifiers, wbemQueryFlagDeep, wbemQueryFlagShallow, wmi.swbemservices_subclassesofasync
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
 - SWbemServices.SubclassesOfAsync
 - ISWbemServices.SubclassesOfAsync
 - ISWbemServices.SubclassesOfAsync
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemServices::SubclassesOfAsync


## -description


The 
<b>SubclassesOfAsync</b> method of the 
<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object returns a collection of subclasses for a specified class. Only use this method for class objects.

This method is called in the asynchronous mode. For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param objWbemSink




### -param strSuperclass [optional]

Specifies a parent class name. Only the classes that are subclasses of this class are returned in the enumerator. If this parameter is blank, and if <i>iFlags</i> is <b>wbemQueryFlagShallow</b>, only the top-level classes are returned (that is, classes that have no parent class). If this parameter is blank, and if <i>iFlags</i> is <b>wbemQueryFlagDeep</b>, all classes within the namespace are returned.


### -param iFlags [optional]

Determines the depth of the call enumeration. The default value for this parameter is <b>wbemQueryFlagDeep</b>. This parameter can accept the following values.



#### wbemQueryFlagShallow (1 (0x1))

Forces the enumeration to include only immediate subclasses of the specified parent class.



#### wbemQueryFlagDeep (0 (0x0))

Default for this parameter. This value forces recursive enumeration into all subclasses that are derived from the specified parent class. The parent class is not returned in the enumeration.



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
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object that returns to the object sink to identify the source of the original asynchronous call. Use this parameter to make multiple asynchronous calls using the same object sink. To use this parameter, create an <b>SWbemNamedValueSet</b> object and use the <a href="https://msdn.microsoft.com/471b23f5-6c53-40e2-a2a9-0798044c9dfb">SWbemNamedValueSet.Add</a> method to add a value that identifies the asynchronous call you are making. This <b>SWbemNamedValueSet</b> object is returned to the object sink and the source of the call can be extracted using the <a href="https://msdn.microsoft.com/ccebe65e-6032-43d5-9004-2247c3b96d6d">SWbemNamedValueSet.Item</a> method. For more information, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


#### - ObjWbemSink

Required. Object sink that receives the subclasses asynchronously. Create a <a href="https://msdn.microsoft.com/a90777ef-fa26-4bfb-b196-c083a0c92a29">SWbemSink</a> object to receive the objects.


#### - objwbemNamedValueSet [optional]

Typically, this parameter is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that is servicing the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


## -returns



This method does not return a value. If successful, the sink receives an 
<a href="https://msdn.microsoft.com/14110ee7-a808-4786-b695-2ce54189d826">OnObjectReady</a> event per instance. After the last instance, the object sink receives an 
<a href="https://msdn.microsoft.com/2723185d-5b8b-4cc7-ada3-51c3275272a9">OnCompleted</a> event.




## -remarks



This call returns immediately.  The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in <i>objWbemSink</i>. To process each object when it arrives, create an <i>objWbemSink</i>.<a href="https://msdn.microsoft.com/14110ee7-a808-4786-b695-2ce54189d826">OnObjectReady</a> event subroutine. After all the objects are returned, you can perform the final processing in your implementation of the  <i>objWbemSink</i>.<a href="https://msdn.microsoft.com/2723185d-5b8b-4cc7-ada3-51c3275272a9">OnCompleted</a> event.

An asynchronous callback allows a non-authenticated user to provide data to the sink. This poses security risks to your scripts and applications. To eliminate the risks, see <a href="https://msdn.microsoft.com/2b839ea9-e1e6-4123-a98a-04ebee907b3b">Setting Security on an Asynchronous Call</a>.




## -see-also




<a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a>



<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a>
 

 

