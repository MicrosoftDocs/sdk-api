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

# DceErrorInqText function


## -description


The 
<b>DceErrorInqText</b> function returns the message text for a status code.


## -parameters




### -param RpcStatus

TBD


### -param ErrorText

Returns the text corresponding to the error code.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RPC_S_OK"></a><a id="rpc_s_ok"></a><dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_S_INVALID_ARG"></a><a id="rpc_s_invalid_arg"></a><dl>
<dt><b>RPC_S_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
Unknown error code.

</td>
</tr>
</table>
 


#### - StatusToConvert

Status code to convert to a text string.


## -returns



This function returns RPC_S_OK if it is successful, or an error code if not.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>DceErrorInqText</b> routine fills the string pointed to by the <i>ErrorText</i> parameter with a null-terminated character string message for a particular status code.



