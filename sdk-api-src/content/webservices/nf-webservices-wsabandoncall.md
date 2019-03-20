---
UID: NF:webservices.WsAbandonCall
title: WsAbandonCall function (webservices.h)
author: windows-sdk-content
description: Abandons a specified call on the specified service proxy.
old-location: wsw\wsabandoncall.htm
tech.root: wsw
ms.assetid: 709af94d-44ad-46af-8771-99d0aba5d77d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WsAbandonCall, WsAbandonCall function [Web Services for Windows], webservices/WsAbandonCall, wsw.wsabandoncall
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - WsAbandonCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsAbandonCall function


## -description



Abandons a specified call  on the specified <a href="https://msdn.microsoft.com/e1a5bf5e-dbc1-43e3-981b-7db4caa08bdc">service proxy</a>. 
            




## -parameters




### -param serviceProxy [in]

Pointer to a <a href="https://msdn.microsoft.com/623766ae-fe82-40f9-93c8-e78fe48bc6d1">WS_SERVICE_PROXY</a> structure representing the service proxy on which to abandon the call.
                


### -param callId [in]

ID of the call to abandon.
                (See the Remarks section.)


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
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The current state of the service proxy is not valid for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> service proxy was passed to the function.

</td>
</tr>
</table>
 




## -remarks



Calls are identified by a call ID. This call ID is associated with the call by the WS_CALL_PROPERTY_CALL_ID  value of the <a href="https://msdn.microsoft.com/d61b6763-9770-4f1d-b16f-c63fc09e8af5">WS_CALL_PROPERTY_ID</a> enumeration. 
              

If the call ID is 0,  all pending calls on the service proxy are abandoned.
              For more information,
                    see the following topics:
                    <ul>
<li>
<a href="https://msdn.microsoft.com/9d6e2441-91de-4108-b1c4-282fbca5fe7c">Client Side Service Operations</a>
</li>
<li>
<a href="https://msdn.microsoft.com/71253dd6-4f59-4acd-b244-c721834ca381">CallAbandonExample</a>
</li>
</ul>


Be aware that the actual I/O associated with the call is not canceled. The service proxy keeps the resources to complete the call even though the call was abandoned. 
            

This results in a consumption of resources that is aggravated if an application continues to abandon calls, as can happen when the server is slow to respond  to the 
                client, and the client application abandons one call only to make the same call again.



