---
UID: NS:schannel._SCHANNEL_SESSION_TOKEN
title: SCHANNEL_SESSION_TOKEN (schannel.h)
description: Specifies whether reconnections are enabled for an authentication session created by calling either the InitializeSecurityContext (Schannel) function or the AcceptSecurityContext (Schannel) function.
helpviewer_keywords: ["PSCHANNEL_SESSION_TOKEN","PSCHANNEL_SESSION_TOKEN structure pointer [Security]","SCHANNEL_SESSION_TOKEN","SCHANNEL_SESSION_TOKEN structure [Security]","SSL_SESSION_DISABLE_RECONNECTS","SSL_SESSION_ENABLE_RECONNECTS","schannel/PSCHANNEL_SESSION_TOKEN","schannel/SCHANNEL_SESSION_TOKEN","security.schannel_session_token"]
old-location: security\schannel_session_token.htm
tech.root: security
ms.assetid: 3c8f5380-eead-4495-8dff-a9561a787930
ms.date: 12/05/2018
ms.keywords: PSCHANNEL_SESSION_TOKEN, PSCHANNEL_SESSION_TOKEN structure pointer [Security], SCHANNEL_SESSION_TOKEN, SCHANNEL_SESSION_TOKEN structure [Security], SSL_SESSION_DISABLE_RECONNECTS, SSL_SESSION_ENABLE_RECONNECTS, schannel/PSCHANNEL_SESSION_TOKEN, schannel/SCHANNEL_SESSION_TOKEN, security.schannel_session_token
req.header: schannel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
targetos: Windows
req.typenames: SCHANNEL_SESSION_TOKEN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SCHANNEL_SESSION_TOKEN
 - schannel/_SCHANNEL_SESSION_TOKEN
 - SCHANNEL_SESSION_TOKEN
 - schannel/SCHANNEL_SESSION_TOKEN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Schannel.h
api_name:
 - SCHANNEL_SESSION_TOKEN
---

# SCHANNEL_SESSION_TOKEN structure


## -description

Specifies whether reconnections are enabled for an authentication session created by calling either the <a href="/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">InitializeSecurityContext (Schannel)</a> function or the <a href="/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext (Schannel)</a>  function.

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

Add a session token to a client context by using this structure as the value of the <i>pInput</i> parameter in a call to the <a href="/windows/desktop/api/sspi/nf-sspi-applycontroltoken">ApplyControlToken</a> function.

This API only applies to Session ID-based reconnects.