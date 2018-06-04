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

# WsRemoveHeader function


## -description


Removes the standard <a href="https://msdn.microsoft.com/4c9b927d-00c7-41e4-bc29-e84a4c23c162">WS_HEADER_TYPE</a> object from a message.
                
                The function is designed to handle types of headers that appear once in the
                message and are targeted at the ultimate receiver.  Headers targeted
                with a role other than ultimate receiver are ignored.

For application-defined header types use the <a href="https://msdn.microsoft.com/def38214-2de9-4a26-93cb-e2f34d8dd6ef">WsRemoveCustomHeader</a> function.


## -parameters




### -param message [in]


                    A pointer to the <b>Message</b> object with the header  to be removed.  
                    The message can be in any state except <b>WS_MESSAGE_STATE_EMPTY</b>.


### -param headerType [in]

Indicates the type of header to be removed.


### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">

                    There are multiple instances of the type of header present in the message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">

                    One or more of the parameters are incorrect.

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




                If a header of the given type exists in the message it is removed.  If the header does not exist, no action is taken
                and the function completes successfully.



