---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWbemCallResult::GetResultObject


## -description


The 
<b>IWbemCallResult::GetResultObject</b> method attempts to retrieve an object from a previous semisynchronous call to 
<a href="https://msdn.microsoft.com/68150273-c4ec-46f1-a3e6-d7169824b69d">IWbemServices::GetObject</a> or 
<a href="https://msdn.microsoft.com/9acba1aa-bcca-416a-863c-704d2e72df07">IWbemServices::ExecMethod</a>. If the object is not yet available, the call returns <b>WBEM_S_TIMEDOUT</b>. Also, before invoking this method to get the resulting object, you may call 
<a href="https://msdn.microsoft.com/5a600fd8-87d8-446d-93da-5b22fd575a11">IWbemCallResult::GetCallStatus</a> until it returns <b>WBEM_S_NO_ERROR</b>, indicating that the original semisynchronous operation is complete.


## -parameters




### -param lTimeout [in]

Specifies the maximum time in milliseconds that this call blocks before returning. If you use the constant <b>WBEM_INFINITE</b> (0xFFFFFFFF), the call blocks until the object is available. If you use 0, the call immediately returns either the object or a status code.


### -param ppResultObject [out]

This parameter cannot be <b>NULL</b>. It receives the copy of the object when it becomes available. You must call <b>IWbemClassObject::Release</b> on the returned object when the object is no longer required. A new object is not returned on error.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.

If the original semisynchronous operation failed (such as when the object was not found, or the method could not be invoked), this method returns the error code that the original function would have returned in its synchronous version.

On error, you can call the COM function <b>GetErrorInfo</b> to obtain more error information.

COM-specific error codes may also be returned if network problems cause you to lose the remote connection to Windows Management.




## -see-also




<a href="https://msdn.microsoft.com/f0aa0233-3b9b-4757-bfdc-26d9fd556ce9">IWbemCallResult</a>



<a href="https://msdn.microsoft.com/9acba1aa-bcca-416a-863c-704d2e72df07">IWbemServices::ExecMethod</a>



<a href="https://msdn.microsoft.com/68150273-c4ec-46f1-a3e6-d7169824b69d">IWbemServices::GetObject</a>
 

 

