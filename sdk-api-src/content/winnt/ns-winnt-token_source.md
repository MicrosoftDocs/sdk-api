---
UID: NS:winnt._TOKEN_SOURCE
title: TOKEN_SOURCE (winnt.h)
description: Identifies the source of an access token.
helpviewer_keywords: ["*PTOKEN_SOURCE","PTOKEN_SOURCE","PTOKEN_SOURCE structure pointer [Security]","TOKEN_SOURCE","TOKEN_SOURCE structure [Security]","_TOKEN_SOURCE","_win32_token_source_str","security.token_source","winnt/PTOKEN_SOURCE","winnt/TOKEN_SOURCE"]
old-location: security\token_source.htm
tech.root: security
ms.assetid: 9c533327-e4a0-4852-828c-622d190b7d1e
ms.date: 12/05/2018
ms.keywords: '*PTOKEN_SOURCE, PTOKEN_SOURCE, PTOKEN_SOURCE structure pointer [Security], TOKEN_SOURCE, TOKEN_SOURCE structure [Security], _TOKEN_SOURCE, _win32_token_source_str, security.token_source, winnt/PTOKEN_SOURCE, winnt/TOKEN_SOURCE'
req.header: winnt.h
req.include-header: Windows.h
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
req.typenames: TOKEN_SOURCE, *PTOKEN_SOURCE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TOKEN_SOURCE
 - winnt/_TOKEN_SOURCE
 - PTOKEN_SOURCE
 - winnt/PTOKEN_SOURCE
 - TOKEN_SOURCE
 - winnt/TOKEN_SOURCE
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
 - TOKEN_SOURCE
---

# TOKEN_SOURCE structure


## -description

The <b>TOKEN_SOURCE</b> structure identifies the source of an <a href="/windows/desktop/SecGloss/a-gly">access token</a>.

## -struct-fields

### -field SourceName

Specifies an 8-byte character string used to identify the source of an access token. This is used to distinguish between such sources as Session Manager, LAN Manager, and RPC Server. A string, rather than a constant, is used to identify the source so users and developers can make extensions to the system, such as by adding other networks, that act as the source of access tokens.

### -field SourceIdentifier

Specifies a locally unique identifier (<a href="/windows/desktop/SecGloss/l-gly">LUID</a>) provided by the source component named by the <b>SourceName</b> member. This value aids the source component in relating context blocks, such as session-control structures, to the token. This value is typically, but not necessarily, an LUID.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a>



<a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_control">TOKEN_CONTROL</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_default_dacl">TOKEN_DEFAULT_DACL</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>



<a href="/windows/desktop/api/winnt/ne-winnt-token_information_class">TOKEN_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_owner">TOKEN_OWNER</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_primary_group">TOKEN_PRIMARY_GROUP</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_statistics">TOKEN_STATISTICS</a>



<a href="/windows/desktop/api/winnt/ne-winnt-token_type">TOKEN_TYPE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_user">TOKEN_USER</a>