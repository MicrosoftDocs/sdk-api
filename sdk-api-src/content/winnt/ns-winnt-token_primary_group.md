---
UID: NS:winnt._TOKEN_PRIMARY_GROUP
title: TOKEN_PRIMARY_GROUP (winnt.h)
description: Specifies a group security identifier (SID) for an access token.
helpviewer_keywords: ["*PTOKEN_PRIMARY_GROUP","PTOKEN_PRIMARY_GROUP","PTOKEN_PRIMARY_GROUP structure pointer [Security]","TOKEN_PRIMARY_GROUP","TOKEN_PRIMARY_GROUP structure [Security]","_TOKEN_PRIMARY_GROUP","_win32_token_primary_group_str","security.token_primary_group","winnt/PTOKEN_PRIMARY_GROUP","winnt/TOKEN_PRIMARY_GROUP"]
old-location: security\token_primary_group.htm
tech.root: security
ms.assetid: d23ebe6c-36a3-434a-a0fa-fcdf50dd19a0
ms.date: 12/05/2018
ms.keywords: '*PTOKEN_PRIMARY_GROUP, PTOKEN_PRIMARY_GROUP, PTOKEN_PRIMARY_GROUP structure pointer [Security], TOKEN_PRIMARY_GROUP, TOKEN_PRIMARY_GROUP structure [Security], _TOKEN_PRIMARY_GROUP, _win32_token_primary_group_str, security.token_primary_group, winnt/PTOKEN_PRIMARY_GROUP, winnt/TOKEN_PRIMARY_GROUP'
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
req.typenames: TOKEN_PRIMARY_GROUP, *PTOKEN_PRIMARY_GROUP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TOKEN_PRIMARY_GROUP
 - winnt/_TOKEN_PRIMARY_GROUP
 - PTOKEN_PRIMARY_GROUP
 - winnt/PTOKEN_PRIMARY_GROUP
 - TOKEN_PRIMARY_GROUP
 - winnt/TOKEN_PRIMARY_GROUP
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
 - TOKEN_PRIMARY_GROUP
---

# TOKEN_PRIMARY_GROUP structure


## -description

The <b>TOKEN_PRIMARY_GROUP</b> structure specifies a group <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) for an <a href="/windows/desktop/SecGloss/a-gly">access token</a>.

## -struct-fields

### -field PrimaryGroup

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure representing a group that will become the primary group of any objects created by a process using this access token. The SID must be one of the group SIDs already in the token.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation">SetTokenInformation</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_control">TOKEN_CONTROL</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_default_dacl">TOKEN_DEFAULT_DACL</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>



<a href="/windows/desktop/api/winnt/ne-winnt-token_information_class">TOKEN_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_owner">TOKEN_OWNER</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_source">TOKEN_SOURCE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_statistics">TOKEN_STATISTICS</a>



<a href="/windows/desktop/api/winnt/ne-winnt-token_type">TOKEN_TYPE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_user">TOKEN_USER</a>