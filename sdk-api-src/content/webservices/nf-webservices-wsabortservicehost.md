---
UID: NF:webservices.WsAbortServiceHost
title: WsAbortServiceHost function
author: windows-driver-content
description: Aborts all current operations on the specified service host.
old-location: wsw\wsabortservicehost.htm
old-project: wsw
ms.assetid: d9405b21-52d2-4d33-b133-f15402dd1d5b
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: WsAbortServiceHost, WsAbortServiceHost function [Web Services for Windows], webservices/WsAbortServiceHost, wsw.wsabortservicehost
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
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WebServices.dll
api_name:
-	WsAbortServiceHost
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsAbortServiceHost function


## -description



Aborts all current operations on the specified <a href="https://msdn.microsoft.com/42e4d24d-5611-4561-b874-6dc3f3f88c73">service host</a>.
             
                




## -parameters




### -param serviceHost [in]

Pointer to a <a href="https://msdn.microsoft.com/1186e3ae-87d0-4d0b-a7cc-cce63dc091e2">WS_SERVICE_HOST</a>  structure representing the service host on which to abort operations.
                


### -param error [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> structure that receives additional error information if the function fails.
                


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">

One or more arguments are invalid.

</td>
</tr>
</table>
 




## -remarks



<b>WsAbortServiceHost</b> aborts all  listeners on the service host, and as a result, no new channels are accepted from the client. All channels currently being used by the service host to service messages are aborted as well. 

If a call is pending and it has a cancel callback registered through the <a href="https://msdn.microsoft.com/3e456814-f70f-47ab-b866-f0b73d5cd35e">WsRegisterOperationForCancel</a> function, the callback is called. However, the runtime still waits for the call to complete. 


           

For more information on registering for cancellation notification,
                see  <a href="https://msdn.microsoft.com/3e456814-f70f-47ab-b866-f0b73d5cd35e">WsRegisterOperationForCancel</a>. 
           



