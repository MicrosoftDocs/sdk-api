---
UID: NF:wbemdisp.ISWbemServicesEx.PutAsync
title: ISWbemServicesEx::PutAsync
author: windows-sdk-content
description: Saves an object asynchronously to a namespace. When successful, this method sends an OnCompleted event to the SWbemSink object that is specified as an input parameter.
old-location: wmi\swbemservicesex_putasync.htm
old-project: WmiSdk
ms.assetid: 27da0c60-6dae-482d-a9bf-1aab016d3ae8
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISWbemServicesEx interface [Windows Management Instrumentation],PutAsync method, ISWbemServicesEx.PutAsync, ISWbemServicesEx::PutAsync, PutAsync, PutAsync method [Windows Management Instrumentation], PutAsync method [Windows Management Instrumentation],ISWbemServicesEx interface, PutAsync method [Windows Management Instrumentation],SWbemServicesEx object, SWbemServicesEx object [Windows Management Instrumentation],PutAsync method, SWbemServicesEx.PutAsync, _hmm_swbemservicesex.putasync, wbemChangeFlagCreateOnly, wbemChangeFlagCreateOrUpdate, wbemChangeFlagUpdateCompatible, wbemChangeFlagUpdateForceMode, wbemChangeFlagUpdateOnly, wbemChangeFlagUpdateSafeMode, wbemFlagReturnImmediately, wbemFlagReturnWhenComplete, wbemFlagUseAmendedQualifiers, wmi.swbemservicesex_putasync
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
 - SWbemServicesEx.PutAsync
 - ISWbemServicesEx.PutAsync
 - ISWbemServicesEx.PutAsync
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemServicesEx::PutAsync


## -description


The 
<b>PutAsync</b> method of the 
<a href="https://msdn.microsoft.com/def514a9-eca4-41de-87cd-c9f964a71f68">SWbemServicesEx</a> object saves an object asynchronously to a namespace. When successful, this method sends an 
<a href="https://msdn.microsoft.com/2723185d-5b8b-4cc7-ada3-51c3275272a9">OnCompleted</a> event to the 
<a href="https://msdn.microsoft.com/a90777ef-fa26-4bfb-b196-c083a0c92a29">SWbemSink</a> object that is specified as an input parameter.

This method is called in the asynchronous mode. For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param objWbemSink

Required. Object sink that receives the objects asynchronously. Create a <a href="https://msdn.microsoft.com/a90777ef-fa26-4bfb-b196-c083a0c92a29">SWbemSink</a> object to receive the objects.


### -param objWbemObject




### -param iFlags [optional]

This parameter determines whether  the call creates or updates the object and whether  the call returns immediately. This parameter can accept the following values.



#### wbemChangeFlagUpdateCompatible (0 (0x0))

Allows a class to be updated when there are no derived classes and  no instances for the class. It also allows updates in all cases when the change is only to unimportant qualifiers, for example, the <b>Description</b> qualifier. This is the default behavior for this call, and is used for compatibility with previous versions of WMI. If the class has instances, the update fails.



#### wbemChangeFlagUpdateSafeMode (32 (0x20))

Allows updates of classes even when there are child classes and the change does not cause conflicts with the child classes. Use this flag when adding a new property to a base class that is not mentioned previously in any of the child classes. If the class has instances, the update fails.



#### wbemChangeFlagUpdateForceMode (64 (0x40))

This flag forces updates of classes when conflicting child classes exist. For example, this flag forces an update when a class qualifier is defined in a child class, and the base class tries to add the same qualifier in conflict with the existing one. In the force mode, this conflict is resolved by deleting the conflicting qualifier in the child class. If the class has instances, the update fails.

The use of the force mode to update a static class causes the deletion of all instances of that class. A forced update on a provider class does not delete instances of the class.



#### wbemChangeFlagCreateOrUpdate (0 (0x0))

Causes the class or instance to be created if it does not exist, or overwritten if it exists already.



#### wbemChangeFlagCreateOnly (2 (0x2))

Used for creation only. The call fails if the class or instance already exists.



#### wbemChangeFlagUpdateOnly (1 (0x1))

Causes this call to update. The class or instance must exist for the call to be successful.



#### wbemFlagReturnImmediately (16 (0x10))

Causes the call to return immediately.



#### wbemFlagReturnWhenComplete (0 (0x0))

Causes this call to block until the query is complete. This flag calls the method in the synchronous mode.



#### wbemFlagUseAmendedQualifiers (131072 (0x20000))

Causes WMI to write class amendment data and the base class definition. For more information, see 
<a href="https://msdn.microsoft.com/01e1cee5-d882-45b6-ac93-68533c2c6c9d">Localizing WMI Class Information</a>.


### -param objWbemNamedValueSet [optional]

Typically, this is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that services the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


### -param objWbemAsyncContext [optional]

An 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object that returns to the object sink to identify the source of the original asynchronous call. Use this parameter to make multiple asynchronous calls using the same object sink. To use this parameter, create an <b>SWbemNamedValueSet</b> object and use the <a href="https://msdn.microsoft.com/471b23f5-6c53-40e2-a2a9-0798044c9dfb">SWbemNamedValueSet.Add</a> method to add a value that identifies the asynchronous call you are making. This <b>SWbemNamedValueSet</b> object is returned to the object sink and the source of the call can be extracted using the <a href="https://msdn.microsoft.com/ccebe65e-6032-43d5-9004-2247c3b96d6d">SWbemNamedValueSet.Item</a> method. For more information, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


#### - ojbWbemObject

Required. The new object to be put in the namespace. This may be a newly created object or a modified object.


## -returns



This method does not return a value. If the call is successful, the 
<a href="https://msdn.microsoft.com/2046dd03-ac2c-49fa-b1ad-a458967709e5">OnObjectPut</a> event of the supplied object sink receives an <a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a> object, which contains the object path of the instance or class that is successfully committed to WMI.




## -remarks



This call returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in <i>objWbemSink</i>. To handle each object when it arrives, create an <i>objWbemSink</i>.<a href="https://msdn.microsoft.com/14110ee7-a808-4786-b695-2ce54189d826">OnObjectReady</a> event subroutine. Any processing done after all the objects arrive is done in a subroutine for the <i>objWbemSink</i>.<a href="https://msdn.microsoft.com/2723185d-5b8b-4cc7-ada3-51c3275272a9">OnCompleted</a> event.

An asynchronous callback allows a non-authenticated user to provide data to the sink. This poses security risks to your scripts and applications. To eliminate the risks, see <a href="https://msdn.microsoft.com/2b839ea9-e1e6-4123-a98a-04ebee907b3b">Setting Security on an Asynchronous Call</a>.



