---
UID: NS:winnt._TOKEN_ORIGIN
title: TOKEN_ORIGIN (winnt.h)
description: Contains information about the origin of the logon session.
helpviewer_keywords: ["*PTOKEN_ORIGIN","PTOKEN_ORIGIN","PTOKEN_ORIGIN structure pointer [Security]","TOKEN_ORIGIN","TOKEN_ORIGIN structure [Security]","_TOKEN_ORIGIN","security.token_origin","winnt/PTOKEN_ORIGIN","winnt/TOKEN_ORIGIN"]
old-location: security\token_origin.htm
tech.root: security
ms.assetid: b613f76a-7ad1-4066-90a1-244974f10219
ms.date: 12/05/2018
ms.keywords: '*PTOKEN_ORIGIN, PTOKEN_ORIGIN, PTOKEN_ORIGIN structure pointer [Security], TOKEN_ORIGIN, TOKEN_ORIGIN structure [Security], _TOKEN_ORIGIN, security.token_origin, winnt/PTOKEN_ORIGIN, winnt/TOKEN_ORIGIN'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: TOKEN_ORIGIN, *PTOKEN_ORIGIN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TOKEN_ORIGIN
 - winnt/_TOKEN_ORIGIN
 - PTOKEN_ORIGIN
 - winnt/PTOKEN_ORIGIN
 - TOKEN_ORIGIN
 - winnt/TOKEN_ORIGIN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - TOKEN_ORIGIN
---

# TOKEN_ORIGIN structure


## -description

The <b>TOKEN_ORIGIN</b> structure contains information about  the origin of the logon session. This structure is used by the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a> function.

## -struct-fields

### -field OriginatingLogonSession

<a href="/windows/desktop/SecGloss/l-gly">Locally unique identifier</a> (LUID) for the <a href="/windows/desktop/SecGloss/l-gly">logon session</a>. If the token  passed to <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a> resulted from a logon using explicit credentials, such as passing name, domain, and password to the  <a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a> function, then this member will contain the ID of the <i>logon session</i> that created it.  If the token resulted from  network authentication, such as a call to <a href="/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext</a>,  or a call to <b>LogonUser</b> with <i>dwLogonType</i> set to LOGON32_LOGON_NETWORK or LOGON32_LOGON_NETWORK_CLEARTEXT, then this member will be zero.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a>