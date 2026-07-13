---
UID: NE:winnt._TOKEN_TYPE
title: TOKEN_TYPE (winnt.h)
description: Contains values that differentiate between a primary token and an impersonation token.
helpviewer_keywords: ["*PTOKEN_TYPE","PTOKEN_TYPE","PTOKEN_TYPE enumeration pointer [Security]","TOKEN_TYPE","TOKEN_TYPE enumeration [Security]","TokenImpersonation","TokenPrimary","_win32_token_type_str","security.token_type","winnt/PTOKEN_TYPE","winnt/TOKEN_TYPE","winnt/TokenImpersonation","winnt/TokenPrimary"]
old-location: security\token_type.htm
tech.root: security
ms.assetid: 51b6717e-3fda-4af4-8995-4ac571eae2fd
ms.date: 12/05/2018
ms.keywords: '*PTOKEN_TYPE, PTOKEN_TYPE, PTOKEN_TYPE enumeration pointer [Security], TOKEN_TYPE, TOKEN_TYPE enumeration [Security], TokenImpersonation, TokenPrimary, _win32_token_type_str, security.token_type, winnt/PTOKEN_TYPE, winnt/TOKEN_TYPE, winnt/TokenImpersonation, winnt/TokenPrimary'
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
req.typenames: TOKEN_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TOKEN_TYPE
 - winnt/_TOKEN_TYPE
 - TOKEN_TYPE
 - winnt/TOKEN_TYPE
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
 - TOKEN_TYPE
---

# TOKEN_TYPE enumeration


## -description

The <b>TOKEN_TYPE</b> enumeration contains values that differentiate between a <a href="/windows/desktop/SecGloss/p-gly">primary token</a> and an <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a>.

## -enum-fields

### -field TokenPrimary:1

Indicates a primary token.

### -field TokenImpersonation

Indicates an impersonation token.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-enumerations">Authorization Enumerations</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_control">TOKEN_CONTROL</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_default_dacl">TOKEN_DEFAULT_DACL</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>



<a href="/windows/desktop/api/winnt/ne-winnt-token_information_class">TOKEN_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_owner">TOKEN_OWNER</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_primary_group">TOKEN_PRIMARY_GROUP</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_source">TOKEN_SOURCE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_statistics">TOKEN_STATISTICS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_user">TOKEN_USER</a>
