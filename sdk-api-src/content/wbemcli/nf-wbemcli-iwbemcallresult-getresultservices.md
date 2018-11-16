---
UID: NF:wbemcli.IWbemCallResult.GetResultServices
title: IWbemCallResult::GetResultServices
author: windows-sdk-content
description: Retrieves the IWbemServices pointer, which results from a semisynchronous call to IWbemServices::OpenNamespace when it becomes available.
old-location: wmi\iwbemcallresult_getresultservices.htm
tech.root: WmiSdk
ms.assetid: 64a4fc4c-f479-4b03-847c-041508e55532
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetResultServices, GetResultServices method [Windows Management Instrumentation], GetResultServices method [Windows Management Instrumentation],IWbemCallResult interface, IWbemCallResult interface [Windows Management Instrumentation],GetResultServices method, IWbemCallResult.GetResultServices, IWbemCallResult::GetResultServices, _hmm_iwbemcallresult_getresultservices, wbemcli/IWbemCallResult::GetResultServices, wmi.iwbemcallresult_getresultservices
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
 - IWbemCallResult.GetResultServices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wbemcli.h
: 
- IWbemCallResult.GetResultServices
: 
---

# IWbemCallResult::GetResultServices


## -description


The 
<b>IWbemCallResult::GetResultServices</b> method  retrieves the 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> pointer, which results from a semisynchronous call to 
<a href="https://msdn.microsoft.com/09ff9078-3d97-432b-8626-62f12b5e3ef4">IWbemServices::OpenNamespace</a> when it becomes available.


## -parameters




### -param lTimeout [in]

The maximum time in milliseconds that this call blocks before it returns. If you use the constant <b>WBEM_INFINITE</b> (0xFFFFFFFF), the call blocks until the interface pointer is available. If you use 0, the call immediately returns either the pointer or a status code.


### -param ppServices [out]

Cannot be <b>NULL</b>. It receives a pointer to the 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> interface requested by the original call to 
<a href="https://msdn.microsoft.com/09ff9078-3d97-432b-8626-62f12b5e3ef4">OpenNamespace</a> when it becomes available The caller must call <a href="_com_iunknown_release">IWbemServices::Release</a>on the returned object when it is no longer required.

On error, a new object is not returned.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

On error, the COM function <a href=" http://go.microsoft.com/fwlink/p/?linkid=119575">GetErrorInfo</a> can be called to obtain more error information.

COM-specific error codes may also be returned if network problems cause you to lose the remote connection to Windows Management.




## -see-also




<a href="https://msdn.microsoft.com/f0aa0233-3b9b-4757-bfdc-26d9fd556ce9">IWbemCallResult</a>



<a href="https://msdn.microsoft.com/09ff9078-3d97-432b-8626-62f12b5e3ef4">IWbemServices::OpenNamespace</a>
 

 

