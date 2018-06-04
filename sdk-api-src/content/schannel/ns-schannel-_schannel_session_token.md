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

# _SCHANNEL_SESSION_TOKEN structure


## -description


Specifies whether reconnections are enabled for an authentication session created by calling either the <a href="https://msdn.microsoft.com/c451089a-d10d-469c-99dd-43d75a6b0b2a">InitializeSecurityContext (Schannel)</a> function or the <a href="https://msdn.microsoft.com/03fd5272-8476-4c93-8590-0d00acf6a130">AcceptSecurityContext (Schannel)</a>  function.


## -struct-fields




### -field dwTokenType

Specifies the type of this structure. Set the value of this member to <b>SCHANNEL_SESSION</b>.


### -field dwFlags

Specifies whether reconnections are to be enabled or disabled. This member must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SSL_SESSION_ENABLE_RECONNECTS"></a><a id="ssl_session_enable_reconnects"></a><dl>
<dt><b>SSL_SESSION_ENABLE_RECONNECTS</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Reconnections are enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="SSL_SESSION_DISABLE_RECONNECTS"></a><a id="ssl_session_disable_reconnects"></a><dl>
<dt><b>SSL_SESSION_DISABLE_RECONNECTS</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Reconnections are disabled.

</td>
</tr>
</table>
 


## -remarks



Add a session token to a client context by using this structure as the value of the <i>pInput</i> parameter in a call to the <a href="https://msdn.microsoft.com/5ce13a05-874c-4e1a-9be8-aed98609791e">ApplyControlToken</a> function.

This API only applies to Session ID-based reconnects.



