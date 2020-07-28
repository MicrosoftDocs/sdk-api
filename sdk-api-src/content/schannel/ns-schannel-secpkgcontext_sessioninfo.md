---
UID: NS:schannel._SecPkgContext_SessionInfo
title: SecPkgContext_SessionInfo (schannel.h)
description: Specifies whether the session is a reconnection and retrieves a value that identifies the session.
helpviewer_keywords: ["*PSecPkgContext_SessionInfo","PSecPkgContext_SessionInfo","PSecPkgContext_SessionInfo structure pointer [Security]","SSL_SESSION_RECONNECT","SecPkgContext_SessionInfo","SecPkgContext_SessionInfo structure [Security]","schannel/PSecPkgContext_SessionInfo","schannel/SecPkgContext_SessionInfo","security.secpkgcontext_sessioninfo"]
old-location: security\secpkgcontext_sessioninfo.htm
tech.root: security
ms.assetid: d7725803-1f4c-4d5d-8c53-81ec24d5a9d8
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_SessionInfo, PSecPkgContext_SessionInfo, PSecPkgContext_SessionInfo structure pointer [Security], SSL_SESSION_RECONNECT, SecPkgContext_SessionInfo, SecPkgContext_SessionInfo structure [Security], schannel/PSecPkgContext_SessionInfo, schannel/SecPkgContext_SessionInfo, security.secpkgcontext_sessioninfo'
f1_keywords:
- schannel/SecPkgContext_SessionInfo
dev_langs:
- c++
req.header: schannel.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Schannel.h
api_name:
- SecPkgContext_SessionInfo
targetos: Windows
req.typenames: SecPkgContext_SessionInfo, *PSecPkgContext_SessionInfo
req.redist: 
ms.custom: 19H1
---

# SecPkgContext_SessionInfo structure


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




<a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-querycontextattributesw">QueryContextAttributes (Schannel)</a>
 

 

