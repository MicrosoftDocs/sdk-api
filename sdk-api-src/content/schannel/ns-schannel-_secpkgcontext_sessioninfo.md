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

# _SecPkgContext_SessionInfo structure


## -description


Specifies whether the session is a reconnection and retrieves a value that identifies the session.


## -struct-fields




### -field dwFlags

Bit flags that specify the type of session. The following value is defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SSL_SESSION_RECONNECT"></a><a id="ssl_session_reconnect"></a><dl>
<dt><b>SSL_SESSION_RECONNECT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The session is a reconnection.

</td>
</tr>
</table>
 


### -field cbSessionId

The size, in bytes, of the <b>rgbSessionId</b> array.


### -field rgbSessionId

An array of up to 32 bytes that identifies the session.


## -see-also




<a href="https://msdn.microsoft.com/0329e525-a743-4e6c-aac4-9f74274dadd2">QueryContextAttributes (Schannel)</a>
 

 

