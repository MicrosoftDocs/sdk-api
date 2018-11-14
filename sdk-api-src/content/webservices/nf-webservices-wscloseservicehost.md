---
UID: NF:webservices.WsCloseServiceHost
title: WsCloseServiceHost function
author: windows-sdk-content
description: Closes down communication with the specified service host.
old-location: wsw\wscloseservicehost.htm
tech.root: wsw
ms.assetid: 46abbcba-72ba-4328-858d-367218f45df3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WsCloseServiceHost, WsCloseServiceHost function [Web Services for Windows], webservices/WsCloseServiceHost, wsw.wscloseservicehost
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsCloseServiceHost
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WsCloseServiceHost
: 
---

# WsCloseServiceHost function


## -description



Closes down communication with the specified <a href="https://msdn.microsoft.com/42e4d24d-5611-4561-b874-6dc3f3f88c73">service host</a>. 
            




## -parameters




### -param serviceHost [in]

Pointer to a <a href="https://msdn.microsoft.com/1186e3ae-87d0-4d0b-a7cc-cce63dc091e2">WS_SERVICE_HOST</a> structure that represents the service host to be closed.
                


### -param asyncContext [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/3c9ffbef-2f5b-42b0-96b1-f17f0ab98ca4">WS_ASYNC_CONTEXT</a> structure containing information for invoking the function asynchronously. Pass <b>NULL</b> to invoke the function synchronously.


### -param error [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> structure  that receives additional error information if the function fails.
                


## -returns



If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_S_ASYNC</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous operation is still pending.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The current state of the service host is not valid for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_OPERATION_TIMED_OUT</b></dt>
</dl>
</td>
<td width="60%">
The operation did not complete within the time allotted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_OPERATION_ABORTED</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>
 




## -remarks



<b>WsCloseServiceHost</b> closes all  listeners on the service host. As a result, no new 
                channels are accepted from the client. However, pending I/O on  channels already accepted 
                is allowed to complete. 
                

This has implications for endpoints configured to run with session-based channel bindings. If a client has an open session with a service on such an endpoint, the 
                closure will not complete until the client closes the session with the service. 
            



