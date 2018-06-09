---
UID: NF:wbemdisp.ISWbemServices.ReferencesToAsync
title: ISWbemServices::ReferencesToAsync
author: windows-sdk-content
description: Returns all association classes or instances that refer to a specific source class or instance.
old-location: wmi\swbemservices_referencestoasync.htm
old-project: WmiSdk
ms.assetid: 2ad66ea1-b8f0-4b6b-b68f-29496afbe4bf
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemServices interface [Windows Management Instrumentation],ReferencesToAsync method, ISWbemServices.ReferencesToAsync, ISWbemServices::ReferencesToAsync, ReferencesToAsync, ReferencesToAsync method [Windows Management Instrumentation], ReferencesToAsync method [Windows Management Instrumentation],ISWbemServices interface, ReferencesToAsync method [Windows Management Instrumentation],SWbemServices object, SWbemServices object [Windows Management Instrumentation],ReferencesToAsync method, SWbemServices.ReferencesToAsync, _hmm_swbemservices.referencestoasync, wbemFlagDontSendStatus, wbemFlagSendStatus, wbemFlagUseAmendedQualifiers, wmi.swbemservices_referencestoasync
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
 - SWbemServices.ReferencesToAsync
 - ISWbemServices.ReferencesToAsync
 - ISWbemServices.ReferencesToAsync
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemServices::ReferencesToAsync


## -description


The 
<b>ReferencesToAsync</b> method of the 
<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object returns all association classes or instances that refer to a specific source class or instance. This method performs the same function that the <a href="https://msdn.microsoft.com/674be546-e7fd-4150-9d7c-2888d24bf1b3">REFERENCES OF</a> WQL query performs.

For more information about the asynchronous mode, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For an explanation of this syntax,  see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param objWbemSink




### -param strObjectPath

Required. String that contains the object path of the source for this method. For more information, see <a href="https://msdn.microsoft.com/01e1cee5-d882-45b6-ac93-68533c2c6c9d">Localizing WMI Class Information</a>.


### -param strResultClass [optional]

String that contains a class name. If specified, this parameter indicates that the returned association objects must belong to or be derived from the class that is specified in this parameter.


### -param strRole [optional]

String that contains a property name. If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role. The role is defined by the name of a specified reference property of an association.


### -param bClassesOnly [optional]

Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes. These are the classes to which the association objects belong. The default value for this parameter is <b>FALSE</b>.


### -param bSchemaOnly [optional]

Boolean value that indicates whether or not the query applies to the schema rather than the data. The default value for this parameter is <b>FALSE</b>. It can only be set to <b>TRUE</b> if the <i>strObjectPath</i> parameter specifies the object path of a class. When set to <b>TRUE</b>, the set of returned endpoints represents classes that are associated with the source class in schema.


### -param strRequiredQualifier [optional]

String that contains a qualifier name. If specified, this parameter indicates that the returned association objects must include the specified qualifier.


### -param iFlags [optional]

Integer that specifies additional flags to the operation. The default for this parameter is <b>wbemFlagBidirectional</b>. This parameter can accept the following values.



#### wbemFlagSendStatus (128 (0x80))

Causes asynchronous calls to send status updates to the 
<a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">OnProgress</a> event handler for the object sink.



#### wbemFlagDontSendStatus (0 (0x0))

Prevents asynchronous calls from sending status updates to the 
<a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">OnProgress</a> event handler for the object sink.



#### wbemFlagUseAmendedQualifiers (131072 (0x20000))

Causes Windows Management Instrumentation (WMI) to return class amendment data along with the base class definition. 
For more information, see <a href="https://msdn.microsoft.com/01e1cee5-d882-45b6-ac93-68533c2c6c9d">Localizing WMI Class Information</a>.


### -param objWbemNamedValueSet [optional]

Typically, this is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that is servicing the request. A provider that supports or requires context information must document the recognized value names, data type of the value, allowed values, and semantics.


### -param objWbemAsyncContext [optional]

This is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object that returns to the object sink to identify the source of the original asynchronous call. Use this parameter to make multiple asynchronous calls using the same object sink. To use this parameter, create an <b>SWbemNamedValueSet</b> object, and use the <a href="https://msdn.microsoft.com/471b23f5-6c53-40e2-a2a9-0798044c9dfb">SWbemNamedValueSet.Add</a> method to add a value that identifies the asynchronous call you are making. This <b>SWbemNamedValueSet</b> object is returned to the object sink, and the source of the call can be extracted using the <a href="https://msdn.microsoft.com/ccebe65e-6032-43d5-9004-2247c3b96d6d">SWbemNamedValueSet.Item</a> method. For more information, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


#### - ObjWbemSink

Required. Object sink that receives the objects asynchronously. Create a <a href="https://msdn.microsoft.com/a90777ef-fa26-4bfb-b196-c083a0c92a29">SWbemSink</a> object to receive the objects.


## -returns



This method does not return a value. If successful, the sink receives an 
<a href="https://msdn.microsoft.com/14110ee7-a808-4786-b695-2ce54189d826">OnObjectReady</a> event per instance. After the last instance, the object sink receives an 
<a href="https://msdn.microsoft.com/2723185d-5b8b-4cc7-ada3-51c3275272a9">OnCompleted</a> event.




## -remarks



This call returns immediately.  The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in <i>objWbemSink</i>. To process each object when it returns, create an <i>objWbemSink</i>.<a href="https://msdn.microsoft.com/14110ee7-a808-4786-b695-2ce54189d826">OnObjectReady</a> event subroutine. After all the objects are returned, you can perform final processing in your implementation of the  <i>objWbemSink</i>.<a href="https://msdn.microsoft.com/2723185d-5b8b-4cc7-ada3-51c3275272a9">OnCompleted</a> event.

An asynchronous callback allows a non-authenticated user to provide data to the sink. This poses security risks to your scripts and applications. To eliminate the risks, see <a href="https://msdn.microsoft.com/2b839ea9-e1e6-4123-a98a-04ebee907b3b">Setting Security on an Asynchronous Call</a>.




## -see-also




<a href="https://msdn.microsoft.com/79f01853-c649-4cbe-b2fa-cff38fb4b733">SWbemObject.Associators_</a>



<a href="https://msdn.microsoft.com/ba02da47-0bb2-40e1-af50-1c42b4be2abd">SWbemObject.References_</a>



<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a>



<a href="https://msdn.microsoft.com/33425b1c-13f5-4c3d-8f8a-2922f3e95264">SWbemServices.AssociatorsOf</a>
 

 

