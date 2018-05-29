---
UID: NF:webservices.WsAbortServiceProxy
title: WsAbortServiceProxy function
author: windows-sdk-content
description: Aborts the service proxy, and cancels any pending I/O on the service proxy.
old-location: wsw\wsabortserviceproxy.htm
old-project: wsw
ms.assetid: 45dc9df4-3a98-446f-b749-809607137fb1
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WsAbortServiceProxy, WsAbortServiceProxy function [Web Services for Windows], webservices/WsAbortServiceProxy, wsw.wsabortserviceproxy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
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
-	WsAbortServiceProxy
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsAbortServiceProxy function


## -description




                Aborts the <a href="https://msdn.microsoft.com/e1a5bf5e-dbc1-43e3-981b-7db4caa08bdc">service proxy</a>, and cancels any pending I/O on the service proxy.
            




## -parameters




### -param serviceProxy [in]


                    Pointer to a <a href="https://msdn.microsoft.com/623766ae-fe82-40f9-93c8-e78fe48bc6d1">WS_SERVICE_PROXY</a> structure representing the service proxy to abort.


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



<b>WsAbortServiceProxy</b> shows the following  behavior depending on the state of service proxy (see the <a href="https://msdn.microsoft.com/82156e64-ae95-4a4a-aaad-e3dd69832c97">WS_SERVICE_PROXY_STATE</a> enumeration for possible states):<ul>
<li>If the service proxy is opening and in the WS_SERVICE_PROXY_STATE_OPENING state, you can call <b>WsAbortServiceProxy</b> to abort the opening operation. The service proxy will
                cancel all pending I/O and transition back to WS_SERVICE_PROXY_STATE_CREATED state.</li>
<li>If the service proxy is already open and in the WS_SERVICE_PROXY_STATE_OPEN state, <b>WsAbortServiceProxy</b> will cause the service proxy to abort all underlying channels and transition to the 
            WS_SERVICE_PROXY_STATE_FAULTED state. Once the abort is initiated, the service proxy will not accept any new calls. The application can call <a href="https://msdn.microsoft.com/034f9c60-5616-4ec7-9773-b34bde2e26c6">WsCloseServiceProxy</a> to close it</li>
<li>If the service proxy is closing and in the WS_SERVICE_PROXY_STATE_CLOSING state, all underlying channels are aborted, and the service proxy tansitions to the WS_SERVICE_PROXY_STATE_CLOSED state. 
</li>
</ul>



                For an example of using this function, see <a href="https://msdn.microsoft.com/c9e727c8-5fa7-47b9-8624-18fe4de79026">ServiceCancellationExample</a>.
           



