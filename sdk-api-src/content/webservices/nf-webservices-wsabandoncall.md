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



