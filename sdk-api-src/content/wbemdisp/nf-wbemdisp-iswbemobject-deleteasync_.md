---
UID: NF:wbemdisp.ISWbemObject.DeleteAsync_
title: ISWbemObject::DeleteAsync_
author: windows-sdk-content
description: The DeleteAsync_ method of SWbemObject asynchronously deletes either the current class or the current instance.
old-location: wmi\swbemobject_deleteasync_.htm
old-project: WmiSdk
ms.assetid: b8d67fa5-5217-422b-acbe-5eea6028deeb
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: DeleteAsync_, DeleteAsync_ method [Windows Management Instrumentation], DeleteAsync_ method [Windows Management Instrumentation],ISWbemObject interface, DeleteAsync_ method [Windows Management Instrumentation],SWbemObject object, ISWbemObject interface [Windows Management Instrumentation],DeleteAsync_ method, ISWbemObject.DeleteAsync_, ISWbemObject::DeleteAsync_, SWbemObject object [Windows Management Instrumentation],DeleteAsync_ method, SWbemObject.DeleteAsync_, _hmm_swbemobject.deleteasync_, wbemFlagDontSendStatus, wbemFlagSendStatus, wmi.swbemobject_deleteasync_
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
 - SWbemObject.DeleteAsync_
 - ISWbemObject.DeleteAsync_
 - ISWbemObject.DeleteAsync_
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObject::DeleteAsync_


## -description


The 
<b>DeleteAsync_</b> method of <a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>  asynchronously deletes either the current class or the current instance. If a dynamic provider supplies the class or instance, sometimes it is not possible to delete this object unless the provider supports class or instance deletion.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param objWbemSink [in]

Object sink that returns the outcome of the delete operation.


### -param iFlags [in, optional]

Integer that determines the behavior of the call. This parameter can accept the following values.



#### wbemFlagSendStatus (128 (0x80))

Causes asynchronous calls to send status updates to the 
<a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">SWbemSink.OnProgress</a> event handler for the object sink.



#### wbemFlagDontSendStatus (0 (0x0))

Prevents asynchronous calls from sending status updates to the 
<a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">OnProgress</a> event handler for the object sink.


### -param objWbemNamedValueSet




### -param objWbemAsyncContext [in, optional]

This is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object that returns to the object sink to identify the source of the original asynchronous call. Use this parameter if you are making multiple asynchronous calls using the same object sink. To use this parameter, create an <b>SWbemNamedValueSet</b> object and use the <a href="https://msdn.microsoft.com/471b23f5-6c53-40e2-a2a9-0798044c9dfb">SWbemNamedValueSet.Add</a> method to add a value that identifies the asynchronous call you are making. This <b>SWbemNamedValueSet</b> object is returned to the object sink and the source of the call can be extracted using the <a href="https://msdn.microsoft.com/ccebe65e-6032-43d5-9004-2247c3b96d6d">SWbemNamedValueSet.Item</a> method. For more information, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


#### - objwbemNamedValueSet [in, optional]

This parameter is typically undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that is servicing the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


## -returns



This method does not return a value. If this call is successful, the result of the delete operation is provided through the supplied object sink.




## -remarks



This call returns immediately.  The  status is returned to the caller through a callback delivered to the sink that is specified in <i>objWbemSink</i>.

An asynchronous callback allows a nonauthenticated user to provide data to the sink. This poses security risks to your scripts and applications. To eliminate the risks, use either semisynchronous communication or synchronous communication.
For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.



