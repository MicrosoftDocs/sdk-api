---
UID: NF:wbemcli.IWbemCallResult.GetCallStatus
title: IWbemCallResult::GetCallStatus
author: windows-sdk-content
description: The IWbemCallResult::GetCallStatus method returns to the user the status of the current outstanding semisynchronous call. When this call returns WBEM_S_NO_ERROR, the original call to the IWbemServices method is complete.
old-location: wmi\iwbemcallresult_getcallstatus.htm
tech.root: WmiSdk
ms.assetid: 5a600fd8-87d8-446d-93da-5b22fd575a11
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetCallStatus, GetCallStatus method [Windows Management Instrumentation], GetCallStatus method [Windows Management Instrumentation],IWbemCallResult interface, IWbemCallResult interface [Windows Management Instrumentation],GetCallStatus method, IWbemCallResult.GetCallStatus, IWbemCallResult::GetCallStatus, _hmm_iwbemcallresult_getcallstatus, wbemcli/IWbemCallResult::GetCallStatus, wmi.iwbemcallresult_getcallstatus
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemcli.h
api_name:
 - IWbemCallResult.GetCallStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemCallResult::GetCallStatus


## -description


The 
<b>IWbemCallResult::GetCallStatus</b> method returns to the user the status of the current outstanding semisynchronous call. When this call returns <b>WBEM_S_NO_ERROR</b>, the original call to the 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> method is complete.


## -parameters




### -param lTimeout [in]

Specifies the maximum time in milliseconds that this call blocks before it returns. If you use the constant <b>WBEM_INFINITE</b> (0xFFFFFFFF), the call blocks until the original semisynchronous call to an 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> method is complete. If you use 0 (zero), the call immediately returns the call status.


### -param plStatus [out]

If <b>WBEM_S_NO_ERROR</b> returns in the HRESULT to this method, this parameter will receive the final result status of a call to one of the 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> methods: 
<a href="https://msdn.microsoft.com/09ff9078-3d97-432b-8626-62f12b5e3ef4">OpenNamespace</a>, 
<a href="https://msdn.microsoft.com/1e07b328-40f7-4e14-bf53-9a5cebfc23f6">PutInstance</a>, 
<a href="https://msdn.microsoft.com/fcb8694e-6bf1-426d-bc1d-18cf9925f1e0">PutClass</a>, 
<a href="https://msdn.microsoft.com/68150273-c4ec-46f1-a3e6-d7169824b69d">GetObject</a>, 
<a href="https://msdn.microsoft.com/f6dfeb1d-1730-4df4-adf7-f27dd9edc54d">DeleteInstance</a>, 
<a href="https://msdn.microsoft.com/1266d93a-776c-481d-b343-826a5c808d24">DeleteClass</a>, or 
<a href="https://msdn.microsoft.com/9acba1aa-bcca-416a-863c-704d2e72df07">ExecMethod</a>. On error, the value pointed to by <i>plStatus</i> will not be used.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.




## -remarks



On error, you can call the COM function <b>GetErrorInfo</b> to obtain more error information. COM-specific error codes may also be returned if network problems cause you to lose the remote connection to Windows Management.

After invoking an 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> method semisynchronously, you can call 
<b>GetCallStatus</b> at any time to determine whether the call is complete. After 
<b>GetCallStatus</b> has returned <b>WBEM_S_NO_ERROR</b>, which indicates completion of the original 
<b>IWbemServices</b> operation, calls to other 
<a href="https://msdn.microsoft.com/f0aa0233-3b9b-4757-bfdc-26d9fd556ce9">IWbemCallResult</a> methods may be required to retrieve the result of the call, according to the following rules:

<ul>
<li>For 
<a href="https://msdn.microsoft.com/09ff9078-3d97-432b-8626-62f12b5e3ef4">IWbemServices::OpenNamespace</a>, the 
<a href="https://msdn.microsoft.com/64a4fc4c-f479-4b03-847c-041508e55532">GetResultServices</a> method must be called to retrieve the new 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> pointer.</li>
<li>For 
<a href="https://msdn.microsoft.com/1e07b328-40f7-4e14-bf53-9a5cebfc23f6">IWbemServices::PutInstance</a>, the 
<a href="https://msdn.microsoft.com/7a022519-c112-42d4-b777-c3828439f7dd">GetResultString</a> method must be called to obtain the object path that was assigned to the object.</li>
<li>For 
<a href="https://msdn.microsoft.com/68150273-c4ec-46f1-a3e6-d7169824b69d">IWbemServices::GetObject</a>, the 
<a href="https://msdn.microsoft.com/06603f26-587f-4aff-8ae3-7f77f9b266f5">GetResultObject</a> method must be called to retrieve the object.</li>
<li>For the 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> methods 
<a href="https://msdn.microsoft.com/f6dfeb1d-1730-4df4-adf7-f27dd9edc54d">DeleteInstance</a>, 
<a href="https://msdn.microsoft.com/1266d93a-776c-481d-b343-826a5c808d24">DeleteClass</a>, and 
<a href="https://msdn.microsoft.com/9acba1aa-bcca-416a-863c-704d2e72df07">ExecMethod</a>, the 
<b>GetCallStatus</b> method is the only call that returns information regarding these operations.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/f0aa0233-3b9b-4757-bfdc-26d9fd556ce9">IWbemCallResult</a>



<a href="https://msdn.microsoft.com/1266d93a-776c-481d-b343-826a5c808d24">IWbemServices::DeleteClass</a>



<a href="https://msdn.microsoft.com/f6dfeb1d-1730-4df4-adf7-f27dd9edc54d">IWbemServices::DeleteInstance</a>



<a href="https://msdn.microsoft.com/9acba1aa-bcca-416a-863c-704d2e72df07">IWbemServices::ExecMethod</a>



<a href="https://msdn.microsoft.com/68150273-c4ec-46f1-a3e6-d7169824b69d">IWbemServices::GetObject</a>



<a href="https://msdn.microsoft.com/09ff9078-3d97-432b-8626-62f12b5e3ef4">IWbemServices::OpenNamespace</a>



<a href="https://msdn.microsoft.com/1e07b328-40f7-4e14-bf53-9a5cebfc23f6">IWbemServices::PutInstance</a>
 

 

