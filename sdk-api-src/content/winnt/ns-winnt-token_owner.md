---
UID: NS:winnt._TOKEN_OWNER
title: TOKEN_OWNER (winnt.h)
description: Contains the default owner security identifier (SID) that will be applied to newly created objects.
helpviewer_keywords: ["*PTOKEN_OWNER","PTOKEN_OWNER","PTOKEN_OWNER structure pointer [Security]","TOKEN_OWNER","TOKEN_OWNER structure [Security]","_TOKEN_OWNER","_win32_token_owner_str","security.token_owner","winnt/PTOKEN_OWNER","winnt/TOKEN_OWNER"]
old-location: security\token_owner.htm
tech.root: security
ms.assetid: 85617d56-ad46-40a3-a335-121f3c8edcc3
ms.date: 12/05/2018
ms.keywords: '*PTOKEN_OWNER, PTOKEN_OWNER, PTOKEN_OWNER structure pointer [Security], TOKEN_OWNER, TOKEN_OWNER structure [Security], _TOKEN_OWNER, _win32_token_owner_str, security.token_owner, winnt/PTOKEN_OWNER, winnt/TOKEN_OWNER'
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
req.typenames: TOKEN_OWNER, *PTOKEN_OWNER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TOKEN_OWNER
 - winnt/_TOKEN_OWNER
 - PTOKEN_OWNER
 - winnt/PTOKEN_OWNER
 - TOKEN_OWNER
 - winnt/TOKEN_OWNER
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
 - TOKEN_OWNER
---

# TOKEN_OWNER structure


## -description

The <b>TOKEN_OWNER</b> structure contains the default owner <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) that will be applied to newly created objects.

## -struct-fields

### -field Owner

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure representing a user who will become the owner of any objects created by a process using this <a href="/windows/desktop/SecGloss/a-gly">access token</a>. The SID must be one of the user or group SIDs already in the token.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation">SetTokenInformation</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_control">TOKEN_CONTROL</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_default_dacl">TOKEN_DEFAULT_DACL</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>



<a href="/windows/desktop/api/winnt/ne-winnt-token_information_class">TOKEN_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_primary_group">TOKEN_PRIMARY_GROUP</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_source">TOKEN_SOURCE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_statistics">TOKEN_STATISTICS</a>



<a href="/windows/desktop/api/winnt/ne-winnt-token_type">TOKEN_TYPE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_user">TOKEN_USER</a>