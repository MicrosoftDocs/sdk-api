---
UID: NS:winnt._TOKEN_STATISTICS
title: TOKEN_STATISTICS (winnt.h)
description: Contains information about an access token.
helpviewer_keywords: ["*PTOKEN_STATISTICS","PTOKEN_STATISTICS","PTOKEN_STATISTICS structure pointer [Security]","TOKEN_STATISTICS","TOKEN_STATISTICS structure [Security]","_TOKEN_STATISTICS","_win32_token_statistics_str","security.token_statistics","winnt/PTOKEN_STATISTICS","winnt/TOKEN_STATISTICS"]
old-location: security\token_statistics.htm
tech.root: security
ms.assetid: 7fcc4a46-1bac-49c1-a239-b466d3bf31d9
ms.date: 12/05/2018
ms.keywords: '*PTOKEN_STATISTICS, PTOKEN_STATISTICS, PTOKEN_STATISTICS structure pointer [Security], TOKEN_STATISTICS, TOKEN_STATISTICS structure [Security], _TOKEN_STATISTICS, _win32_token_statistics_str, security.token_statistics, winnt/PTOKEN_STATISTICS, winnt/TOKEN_STATISTICS'
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
req.typenames: TOKEN_STATISTICS, *PTOKEN_STATISTICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TOKEN_STATISTICS
 - winnt/_TOKEN_STATISTICS
 - PTOKEN_STATISTICS
 - winnt/PTOKEN_STATISTICS
 - TOKEN_STATISTICS
 - winnt/TOKEN_STATISTICS
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
 - TOKEN_STATISTICS
---

# TOKEN_STATISTICS structure


## -description

The <b>TOKEN_STATISTICS</b> structure contains information about an <a href="/windows/desktop/SecGloss/a-gly">access token</a>. An application can retrieve this information by calling the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a> function.

## -struct-fields

### -field TokenId

Specifies a locally unique identifier (<a href="/windows/desktop/SecGloss/l-gly">LUID</a>) that identifies this instance of the token object.

### -field AuthenticationId

Specifies an LUID assigned to the <a href="/windows/desktop/SecGloss/s-gly">session</a> this token represents. There can be many tokens representing a single <a href="/windows/desktop/SecGloss/l-gly">logon session</a>.

### -field ExpirationTime

Specifies the time at which this token expires. Expiration times for access tokens are not currently supported.

### -field TokenType

Specifies a <a href="/windows/desktop/api/winnt/ne-winnt-token_type">TOKEN_TYPE</a> enumeration type indicating whether the token is a <a href="/windows/desktop/SecGloss/p-gly">primary</a> or <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a>.

### -field ImpersonationLevel

Specifies a <a href="/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a> enumeration type indicating the impersonation level of the token. This member is valid only if the <b>TokenType</b> is TokenImpersonation.

### -field DynamicCharged

Specifies the amount, in bytes, of memory allocated for storing default protection and a primary group identifier.

### -field DynamicAvailable

Specifies the portion of memory allocated for storing default protection and a primary group identifier not already in use. This value is returned as a count of free bytes.

### -field GroupCount

Specifies the number of supplemental group <a href="/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs) included in the token.

### -field PrivilegeCount

Specifies the number of privileges included in the token.

### -field ModifiedId

Specifies an LUID that changes each time the token is modified. An application can use this value as a test of whether a <a href="/windows/desktop/SecGloss/s-gly">security context</a> has changed since it was last used.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a>



<a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a>



<a href="/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_control">TOKEN_CONTROL</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_default_dacl">TOKEN_DEFAULT_DACL</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>



<a href="/windows/desktop/api/winnt/ne-winnt-token_information_class">TOKEN_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_owner">TOKEN_OWNER</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_primary_group">TOKEN_PRIMARY_GROUP</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_source">TOKEN_SOURCE</a>



<a href="/windows/desktop/api/winnt/ne-winnt-token_type">TOKEN_TYPE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_user">TOKEN_USER</a>