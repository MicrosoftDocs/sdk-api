---
UID: NF:wbemdisp.ISWbemObject.ReferencesAsync_
title: ISWbemObject::ReferencesAsync_
author: windows-sdk-content
description: The ReferencesAsync_ method of SWbemObject supplies a collection of all association classes or instances that refer to the current object. This method performs the same function that the WQL REFERENCES OF query performs.
old-location: wmi\swbemobject_referencesasync_.htm
old-project: WmiSdk
ms.assetid: 44989726-3f68-453b-b9f5-e76fb0fbb152
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ISWbemObject interface [Windows Management Instrumentation],ReferencesAsync_ method, ISWbemObject.ReferencesAsync_, ISWbemObject::ReferencesAsync_, ReferencesAsync_, ReferencesAsync_ method [Windows Management Instrumentation], ReferencesAsync_ method [Windows Management Instrumentation],ISWbemObject interface, ReferencesAsync_ method [Windows Management Instrumentation],SWbemObject object, SWbemObject object [Windows Management Instrumentation],ReferencesAsync_ method, SWbemObject.ReferencesAsync_, _hmm_swbemobject.referencesasync_, wbemFlagDontSendStatus, wbemFlagSendStatus, wbemFlagUseAmendedQualifiers, wmi.swbemobject_referencesasync_
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
 - SWbemObject.ReferencesAsync_
 - ISWbemObject.ReferencesAsync_
 - ISWbemObject.ReferencesAsync_
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObject::ReferencesAsync_


## -description


The 
<b>ReferencesAsync_</b> method of <a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>  supplies a collection of all association classes or instances that refer to the current object. This method performs the same function that the WQL <a href="https://msdn.microsoft.com/674be546-e7fd-4150-9d7c-2888d24bf1b3">REFERENCES OF</a> query performs.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param objWbemSink [in]

Required. Object sink that receives the objects asynchronously.


### -param strResultClass [in, optional]

String that contains a class name. If specified, this parameter indicates that the returned association objects must belong to or be derived from the class specified in this parameter.


### -param strRole [in, optional]

String that contains a property name. If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role. The name of a specified reference property defines the role  of an association.


### -param bClassesOnly [in, optional]

Boolean value that indicates whether or not a list of class names should be returned—rather than actual instances of the classes. These are the classes to which the association objects belong. The default value for this parameter is <b>FALSE</b>.


### -param bSchemaOnly [in, optional]

Boolean value that indicates whether or not the query applies to the schema rather than the data. The default value for this parameter is <b>FALSE</b>. It can only be set to <b>TRUE</b> if the object on which this method is invoked is a class. When set to <b>TRUE</b>, the set of returned endpoints represents classes that are suitably associated with the source class in the schema.


### -param strRequiredQualifier [in, optional]

String that contains a qualifier name. If specified, this parameter indicates that the returned association objects must include the specified qualifier.


### -param iFlags [in, optional]

Integer specifying additional flags to the operation. This parameter can accept the following values.



#### wbemFlagSendStatus (128 (0x80))

Causes asynchronous calls to send status updates to the 
<a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">SWbemSink.OnProgress</a> event handler for the object sink.



#### wbemFlagDontSendStatus (0 (0x0))

Prevents asynchronous calls from sending status updates to the 
<a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">OnProgress</a> event handler for the object sink.



#### wbemFlagUseAmendedQualifiers (131072 (0x20000))

Causes Windows Management Instrumentation (WMI) to return class amendment data with the base class definition. 
For more information, see <a href="https://msdn.microsoft.com/01e1cee5-d882-45b6-ac93-68533c2c6c9d">Localizing WMI Class Information</a>.


### -param objWbemNamedValueSet




### -param objWbemAsyncContext [in, optional]

This is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object that returns to the object sink to identify the source of the original asynchronous call. Use this parameter if you are making multiple asynchronous calls using the same object sink. To use this parameter, create an SWbemNamedValueSet object, and use the <a href="https://msdn.microsoft.com/471b23f5-6c53-40e2-a2a9-0798044c9dfb">SWbemNamedValueSet.Add</a> method to add a value that identifies the asynchronous call you are making. This SWbemNamedValueSet object is returned to the object sink and the source of the call can be extracted using the <a href="https://msdn.microsoft.com/ccebe65e-6032-43d5-9004-2247c3b96d6d">SWbemNamedValueSet.Item</a> method. For more information, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


#### - objwbemNamedValueSet [in, optional]

Typically, this is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that is servicing the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


## -returns



This method does not return a value. If successful, the sink receives an 
<a href="https://msdn.microsoft.com/14110ee7-a808-4786-b695-2ce54189d826">OnObjectReady</a> event per instance. After the last instance, the object sink  receives an 
<a href="https://msdn.microsoft.com/2723185d-5b8b-4cc7-ada3-51c3275272a9">OnCompleted</a> event.




## -remarks



This call returns immediately.  The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in <i>objWbemSink</i>. To process each object when it arrives, create an <i>objWbemSink</i>.<a href="https://msdn.microsoft.com/14110ee7-a808-4786-b695-2ce54189d826">OnObjectReady</a> event subroutine. After all the objects are returned, you can perform final processing in your implementation of the  <i>objWbemSink</i>.<a href="https://msdn.microsoft.com/2723185d-5b8b-4cc7-ada3-51c3275272a9">OnCompleted</a> event.

An asynchronous callback allows a non-authenticated user to provide data to the sink. This poses security risks to your scripts and applications. To eliminate the risks, use either semisynchronous communication or synchronous communication.
For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For more information about the REFERENCES OF associated WQL query, source instances, and association objects, see 
<a href="https://msdn.microsoft.com/d6bd9643-523d-4d81-8bf1-da52ccc7524d">ASSOCIATORS OF Statement</a>.




## -see-also




<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>



<a href="https://msdn.microsoft.com/79f01853-c649-4cbe-b2fa-cff38fb4b733">SWbemObject.Associators_</a>



<a href="https://msdn.microsoft.com/a78e6701-6779-4a02-b811-23b2da4f4167">SWbemServices.AssociatorsOf</a>



<a href="https://msdn.microsoft.com/33425b1c-13f5-4c3d-8f8a-2922f3e95264">SWbemServices.ReferencesTo</a>



<a href="https://msdn.microsoft.com/2ad66ea1-b8f0-4b6b-b68f-29496afbe4bf">SWbemServices.ReferencesToAsync</a>
 

 

