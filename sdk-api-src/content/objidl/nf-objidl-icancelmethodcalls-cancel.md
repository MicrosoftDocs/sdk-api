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

# ICancelMethodCalls::Cancel


## -description


Requests that a method call be canceled.


## -parameters




### -param ulSeconds [in]

The number of seconds to wait for the server to complete the outbound call after the client requests cancellation.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The cancellation request was made.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_CALL_CANCELED</b></dt>
</dl>
</td>
<td width="60%">
The call was already canceled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_CANCEL_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
Call cancellation is not enabled on the thread that is processing the call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_E_CALL_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The call was completed during the timeout interval.


</td>
</tr>
</table>
 




## -remarks



The <b>Cancel</b> method only issues a cancel request. A return value of S_OK does not mean that the call was canceled, only that an attempt was made to cancel the call. The behavior of the cancel object on receiving a cancel request is entirely at the discretion of the implementer.

If a method that returns an <b>HRESULT</b> is canceled, the return value will be RPC_S_CALL_CANCELED.




## -see-also




<a href="https://msdn.microsoft.com/5e31f706-1c9c-4510-845c-4e47093780a1">ICancelMethodCalls</a>
 

 

