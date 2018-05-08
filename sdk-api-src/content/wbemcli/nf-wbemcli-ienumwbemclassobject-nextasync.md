---
UID: NF:wbemcli.IEnumWbemClassObject.NextAsync
title: IEnumWbemClassObject::NextAsync
author: windows-driver-content
description: Use the NextAsync method when a controlled asynchronous retrieval of objects to a sink is required.
old-location: wmi\ienumwbemclassobject_nextasync.htm
old-project: WmiSdk
ms.assetid: 1ff82982-a2d7-4618-8488-9e4b7628012d
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IEnumWbemClassObject interface [Windows Management Instrumentation],NextAsync method, IEnumWbemClassObject.NextAsync, IEnumWbemClassObject::NextAsync, NextAsync, NextAsync method [Windows Management Instrumentation], NextAsync method [Windows Management Instrumentation],IEnumWbemClassObject interface, _hmm_ienumwbemclassobject_nextasync, wbemcli/IEnumWbemClassObject::NextAsync, wmi.ienumwbemclassobject_nextasync
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WMI_OBJ_TEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fastprox.dll
api_name:
-	IEnumWbemClassObject.NextAsync
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IEnumWbemClassObject::NextAsync


## -description


Use the <b>NextAsync</b> method when a controlled asynchronous retrieval of objects to a sink is required. Normal asynchronous retrieval, such as a call to 
<a href="https://msdn.microsoft.com/d8b55500-d84c-431b-93c6-99d1f1b845c3">IWbemServices::ExecQueryAsync</a>, results in uncontrolled delivery of objects to the caller's implementation of 
<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a>. This method is helpful for cases where a component controls object delivery.


## -parameters




### -param uCount [in]

Number of objects being requested.


### -param pSink [in]

Sink to receive the objects. The sink must be implemented by the caller. As each batch of objects is requested, they are delivered to the <i>pSink</i> parameter of the 
      <a href="https://msdn.microsoft.com/96756b27-cbcf-47ce-a8c8-88795a81edde">Indicate</a> method followed by a final call to the <i>pSink</i>
      parameter of the <a href="https://msdn.microsoft.com/e47e8cd9-4e80-45c4-b1f0-2f68aea4eb7b">SetStatus</a> method. If the sink is going to be used to deliver objects, this method returns <b>WBEM_S_NO_ERROR</b>, even if the number of objects to be delivered is less than requested. However, if there are no more objects remaining, then the <i>pSink</i> parameter is ignored (no calls to the <i>pSink</i>
      parameter of <b>SetStatus</b> are made). Instead, this method returns <b>WBEM_S_FALSE</b>.


## -returns



The 
<b>NextAsync</b> method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -remarks



A call to the COM function <a href=" http://go.microsoft.com/fwlink/p/?linkid=119575">GetErrorInfo</a> provides more information about the error. COM-specific error codes may also be returned if network problems cause you to lose the remote connection to Windows Management.

This call returns immediately and delivery to the sink occurs in the background. If multiple calls are made to this method from one or more threads, they are logically queued and the order of calls and object delivery is preserved. Multiple calls made to this method from one or more threads block do not return until all the sink objects related to previous calls to this method have been serviced. A call to 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a> does not affect delivery of objects currently in progress as a result of previous calls. The 
<b>Reset</b> method only causes new calls to start at the beginning of the object sequence.

If the number of requested objects is immediately available, the function returns <b>WBEM_S_NO_ERROR</b>. If less than the number of requested objects are available, the available objects are returned and <b>WBEM_S_NO_ERROR</b> are returned. The remainder of the objects are delivered by the user-supplied sink.

As the objects become available, the caller's implementation of 
<a href="https://msdn.microsoft.com/96756b27-cbcf-47ce-a8c8-88795a81edde">IWbemObjectSink::Indicate</a> is called zero or more times to deliver the objects. This is followed by a call to 
<a href="https://msdn.microsoft.com/e47e8cd9-4e80-45c4-b1f0-2f68aea4eb7b">IWbemObjectSink::SetStatus</a> with a value of <b>WBEM_S_NO_ERROR</b> if <i>uCount</i> items are returned.

If fewer objects are available than the number requested, <a href="https://msdn.microsoft.com/96756b27-cbcf-47ce-a8c8-88795a81edde">Indicate</a> is called for those objects that are available. <a href="https://msdn.microsoft.com/e47e8cd9-4e80-45c4-b1f0-2f68aea4eb7b">SetStatus</a> is then called with a value of <b>WBEM_S_FALSE</b>, or the error code if an error occurred.

If the requested number of objects is delivered, the final object is followed by a call to <a href="https://msdn.microsoft.com/e47e8cd9-4e80-45c4-b1f0-2f68aea4eb7b">SetStatus</a> with a status code of <b>WBEM_S_NO_ERROR</b>. If the enumeration completes before the requested number of objects can be delivered, the <b>SetStatus</b> method has a status code of <b>WBEM_S_FALSE</b>.

If there are no available objects, <a href="https://msdn.microsoft.com/96756b27-cbcf-47ce-a8c8-88795a81edde">Indicate</a> is not called. However, a final call to <a href="https://msdn.microsoft.com/e47e8cd9-4e80-45c4-b1f0-2f68aea4eb7b">SetStatus</a> always occurs to indicate the status of the entire operation.

Because the callback might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication. If you require asynchronous communication, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For more information about using methods semisynchronously, see <a href="https://msdn.microsoft.com/8bde633b-b04a-4a21-82ce-f5aab1d32d95">IEnumWbemClassObject::Next</a> and <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.



