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
<a href="https://msdn.microsoft.com/09ff9078-3d97-432b-8626-62f12b5e3ef4">OpenNamespace</a> when it becomes available The caller must call <a href="_com_iunknown_release">IWbemServices::Release</a>
      on the returned object when it is no longer required.

On error, a new object is not returned.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

On error, the COM function <a href=" http://go.microsoft.com/fwlink/p/?linkid=119575">GetErrorInfo</a> can be called to obtain more error information.

COM-specific error codes may also be returned if network problems cause you to lose the remote connection to Windows Management.




## -see-also




<a href="https://msdn.microsoft.com/f0aa0233-3b9b-4757-bfdc-26d9fd556ce9">IWbemCallResult</a>



<a href="https://msdn.microsoft.com/09ff9078-3d97-432b-8626-62f12b5e3ef4">IWbemServices::OpenNamespace</a>
 

 

