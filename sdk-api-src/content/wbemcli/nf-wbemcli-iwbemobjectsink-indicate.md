---
UID: NF:wbemcli.IWbemObjectSink.Indicate
title: IWbemObjectSink::Indicate
author: windows-sdk-content
description: Called by a source to provide a notification.
old-location: wmi\iwbemobjectsink_indicate.htm
old-project: WmiSdk
ms.assetid: 96756b27-cbcf-47ce-a8c8-88795a81edde
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IWbemObjectSink interface [Windows Management Instrumentation],Indicate method, IWbemObjectSink.Indicate, IWbemObjectSink::Indicate, IWbemObjectSinkEx interface [Windows Management Instrumentation],Indicate method, IWbemObjectSinkEx::Indicate, Indicate, Indicate method [Windows Management Instrumentation], Indicate method [Windows Management Instrumentation],IWbemObjectSink interface, Indicate method [Windows Management Instrumentation],IWbemObjectSinkEx interface, _hmm_iwbemobjectsink_indicate, wbemcli/IWbemObjectSink::Indicate, wbemcli/IWbemObjectSinkEx::Indicate, wmi.iwbemobjectsink_indicate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemcli.h
req.include-header: Wbemidl.h
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
req.type-library: 
tech.root: 
req.typenames: WMI_OBJ_TEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fastprox.dll
api_name:
 - IWbemObjectSink.Indicate
 - IWbemObjectSinkEx.Indicate
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemObjectSink::Indicate


## -description


The 
<b>Indicate</b> method is called by a source to provide a notification. Typically, WMI calls the client implementation of this interface after the client executes one of the asynchronous methods of 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a>. In other cases, various types of providers call an implementation exported by WMI to deliver events. Therefore, client code may have to implement this interface in some cases, and use a different component's implementation in other cases.

Use this interface and method in conjunction with the asynchronous methods of the 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> interface.

Clients and providers must implement this interface to receive notifications or to execute the asynchronous methods of 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a>. For more information, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


## -parameters




### -param lObjectCount [in]

Number of objects in the following array of pointers.


### -param apObjArray






#### - ppObjArray [in]

Array of pointers to 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> interfaces. The array memory itself is read-only, and is owned by the caller of the method. Because this is an in parameter, the implementation has the option of calling <a href="https://msdn.microsoft.com/en-us/library/ms691379(v=VS.85).aspx">IWbemClassObject::AddRef</a> on any object pointer in the array and holding it before returning if the objects will be used after the method has returned, in accordance with COM rules. If the objects are only used for the duration of the 
<b>Indicate</b> call, then you do not need to call <b>AddRef</b> on each object pointer.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -remarks



When implementing an event subscription sink (<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a> or <a href="https://msdn.microsoft.com/dd076dd0-ed39-47a2-86fb-a595baf3f464">IWbemEventSink</a>), do  not call into WMI from within the <b>Indicate</b>  method on the sink object.  For example, calling <a href="https://msdn.microsoft.com/803a7831-1e3d-4940-8d2b-1a74dd16f51a">IWbemServices::CancelAsyncCall</a>  from within an implementation of <b>Indicate</b> can interfere with the WMI state. To cancel an event subscription, set a flag and call <b>IWbemServices::CancelAsyncCall</b> from another thread or object. For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.

Sink implementations should process the event notification within 100 MSEC because the WMI thread that delivers the event notification cannot do other work until the sink object has completed processing. If the notification requires a large amount of processing, the sink can use an internal queue for another thread to handle the processing.

When an event provider calls 
<b>Indicate</b> to provide an event, the call can fail with <b>WBEM_E_SERVER_TOO_BUSY</b>. The provider can choose to respond to this message by re-firing the event.

<div class="alert"><b>Note</b>  Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.  For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a>



<a href="https://msdn.microsoft.com/e47e8cd9-4e80-45c4-b1f0-2f68aea4eb7b">IWbemObjectSink::SetStatus</a>



<a href="https://msdn.microsoft.com/f22b21f8-5191-480d-8471-3d5fc82ba060">IWbemObjectSinkEx</a>



<a href="https://msdn.microsoft.com/d8b55500-d84c-431b-93c6-99d1f1b845c3">IWbemServices::ExecQueryAsync</a>
 

 

