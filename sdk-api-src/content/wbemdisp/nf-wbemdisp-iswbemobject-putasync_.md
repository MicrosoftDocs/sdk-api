---
UID: NF:wbemdisp.ISWbemObject.PutAsync_
title: ISWbemObject::PutAsync_
author: windows-sdk-content
description: The PutAsync_ method of SWbemObject asynchronously creates or updates an instance or class object to Windows Management Instrumentation (WMI).
old-location: wmi\swbemobject_putasync_.htm
old-project: WmiSdk
ms.assetid: ff738412-fcca-4e4a-a178-0d1d391ec99b
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ISWbemObject interface [Windows Management Instrumentation],PutAsync_ method, ISWbemObject.PutAsync_, ISWbemObject::PutAsync_, PutAsync_, PutAsync_ method [Windows Management Instrumentation], PutAsync_ method [Windows Management Instrumentation],ISWbemObject interface, PutAsync_ method [Windows Management Instrumentation],SWbemObject object, SWbemObject object [Windows Management Instrumentation],PutAsync_ method, SWbemObject.PutAsync_, WbemChangeFlagUpdateForceMode, _hmm_swbemobject.putasync_, wbemChangeFlagCreateOnly, wbemChangeFlagCreateOrUpdate, wbemChangeFlagUpdateCompatible, wbemChangeFlagUpdateOnly, wbemChangeFlagUpdateSafeMode, wbemFlagDontSendStatus, wbemFlagReturnImmediately, wbemFlagReturnWhenComplete, wbemFlagSendStatus, wbemFlagUseAmendedQualifiers, wmi.swbemobject_putasync_
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
 - SWbemObject.PutAsync_
 - ISWbemObject.PutAsync_
 - ISWbemObject.PutAsync_
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObject::PutAsync_


## -description


The 
<b>PutAsync_</b> method of <a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>  asynchronously creates or updates an instance or class object to Windows Management Instrumentation (WMI). You can use this method after you modify any properties or methods in <b>SWbemObject</b>, and your changes are written to WMI.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param objWbemSink [in]

Required. Object sink that asynchronously receives the result of the <b>put</b> operation.


### -param iFlags [in, optional]

Determines if the call creates or updates the class or instance and if the call returns immediately. This parameter can accept the following values.



#### wbemChangeFlagUpdateCompatible (0 (0x0))

Allows a class to be updated if there are no derived classes and there are no instances for that class. It also allows updates in all cases if the change is just to unimportant qualifiers (for example the <b>Description</b> qualifier). This is the default behavior for this call and is used for compatibility with previous versions of WMI. If the class has instances the update fails.



#### wbemChangeFlagUpdateSafeMode (32 (0x20))

Allows updates of classes, even if there are child classes, if the change does not cause conflicts with child classes. You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes. If the class has instances the update fails.



#### WbemChangeFlagUpdateForceMode (64 (0x40))

Forces updates of classes when conflicting child classes exist. For example, this flag forces an update if a class qualifier was defined in a child class, and the base class attempts to add the same qualifier in conflict with the existing one. In force mode this conflict is resolved by deleting the conflicting qualifier in the child class. If the class has instances the update fails.

Using force mode to update a static class results in the deletion of all instances of that class. A forced update on a provider class does not delete instances of the class.



#### wbemChangeFlagCreateOrUpdate (0 (0x0))

Causes the class or instance to be created if it does not exist or overwritten if it exists already.



#### wbemChangeFlagCreateOnly (2 (0x2))

Used for creation only. The call fails if the class or instance already exists.



#### wbemChangeFlagUpdateOnly (1 (0x1))

Causes this call to update. The class or instance must exist for the call to be successful.



#### wbemFlagReturnImmediately (16 (0x10))

Causes the call to return immediately.



#### wbemFlagReturnWhenComplete (0 (0x0))

Causes this call to block until the query has completed.



#### wbemFlagSendStatus (128 (0x80))

Causes asynchronous calls to send status updates to the 
<a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">SWbemSink.OnProgress</a> event handler for the object sink.



#### wbemFlagDontSendStatus (0 (0x0))

Prevents asynchronous calls from sending status updates to the 
<a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">OnProgress</a> event handler for the object sink.



#### wbemFlagUseAmendedQualifiers (131072 (0x20000))

Causes WMI to write class amendment data along with the base class definition. 
For more information about amended qualifiers, see <a href="https://msdn.microsoft.com/01e1cee5-d882-45b6-ac93-68533c2c6c9d">Localizing WMI Class Information</a>.


### -param objWbemNamedValueSet [in, optional]

Typically, this is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that is servicing the request. A provider that supports or requires this information must document the recognized value names, data type of the value, allowed values, and semantics.


### -param objWbemAsyncContext [in, optional]

This is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object that returns to the object sink to identify the source of the original asynchronous call. Use this parameter if you are making multiple asynchronous calls using the same object sink. To use this parameter, create an <b>SWbemNamedValueSet</b> object and use the <a href="https://msdn.microsoft.com/471b23f5-6c53-40e2-a2a9-0798044c9dfb">SWbemNamedValueSet.Add</a> method to add a value that identifies the asynchronous call you are making. This <b>SWbemNamedValueSet</b> object is returned to the object sink and the source of the call can be extracted using the <a href="https://msdn.microsoft.com/ccebe65e-6032-43d5-9004-2247c3b96d6d">SWbemNamedValueSet.Item</a> method. For more information, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


## -returns



This method does not return a value. If the call is successful, the 
<a href="https://msdn.microsoft.com/2046dd03-ac2c-49fa-b1ad-a458967709e5">OnObjectPut</a> event of the supplied object sink receives an 
<a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a> object, containing the object path of the instance or class that is successfully committed to WMI.




## -remarks



This call returns immediately, and the result of the <b>put</b> operation is returned to the caller through callbacks delivered to the sink that is specified in <i>objWbemSink</i>. Implement the <i>objWbemSink</i>. <a href="https://msdn.microsoft.com/2046dd03-ac2c-49fa-b1ad-a458967709e5">OnObjectPut</a>  method to obtain the object path of the instance or class that is written to the WMI repository. For more information about sink methods, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

An asynchronous callback allows a non-authenticated user to provide data to the sink. This poses security risks to your scripts and applications. To eliminate the risks, use semisynchronous or synchronous communication.
For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.




## -see-also




<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>



<a href="https://msdn.microsoft.com/60123963-31be-4112-9d06-611b4c599fd4">SWbemObjectPath.Class</a>



<a href="https://msdn.microsoft.com/2ddcfffa-a7b4-4fd6-926d-411de27f6212">SWbemProperty</a>



<a href="https://msdn.microsoft.com/b5dbe98a-e1d8-4679-a563-c88760d08b79">SWbemQualifier</a>
 

 

