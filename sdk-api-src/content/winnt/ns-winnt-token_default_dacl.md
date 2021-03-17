---
UID: NS:winnt._TOKEN_DEFAULT_DACL
title: TOKEN_DEFAULT_DACL (winnt.h)
description: Specifies a discretionary access control list (DACL).
helpviewer_keywords: ["*PTOKEN_DEFAULT_DACL","PTOKEN_DEFAULT_DACL","PTOKEN_DEFAULT_DACL structure pointer [Security]","TOKEN_DEFAULT_DACL","TOKEN_DEFAULT_DACL structure [Security]","_TOKEN_DEFAULT_DACL","_win32_token_default_dacl_str","security.token_default_dacl","winnt/PTOKEN_DEFAULT_DACL","winnt/TOKEN_DEFAULT_DACL"]
old-location: security\token_default_dacl.htm
tech.root: security
ms.assetid: 29fb738f-1ecd-4b72-9aea-64698cd74c12
ms.date: 12/05/2018
ms.keywords: '*PTOKEN_DEFAULT_DACL, PTOKEN_DEFAULT_DACL, PTOKEN_DEFAULT_DACL structure pointer [Security], TOKEN_DEFAULT_DACL, TOKEN_DEFAULT_DACL structure [Security], _TOKEN_DEFAULT_DACL, _win32_token_default_dacl_str, security.token_default_dacl, winnt/PTOKEN_DEFAULT_DACL, winnt/TOKEN_DEFAULT_DACL'
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
req.typenames: TOKEN_DEFAULT_DACL, *PTOKEN_DEFAULT_DACL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TOKEN_DEFAULT_DACL
 - winnt/_TOKEN_DEFAULT_DACL
 - PTOKEN_DEFAULT_DACL
 - winnt/PTOKEN_DEFAULT_DACL
 - TOKEN_DEFAULT_DACL
 - winnt/TOKEN_DEFAULT_DACL
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
 - TOKEN_DEFAULT_DACL
---

# TOKEN_DEFAULT_DACL structure


## -description

The <b>TOKEN_DEFAULT_DACL</b> structure specifies a <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL).

## -struct-fields

### -field DefaultDacl

A pointer to an <a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> structure assigned by default to any objects created by the user. The user is represented by the <a href="/windows/desktop/SecGloss/a-gly">access token</a>.

## -remarks

The <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a> function retrieves the default DACL for an access token, in the form of a <b>TOKEN_DEFAULT_DACL</b> structure. This structure is also used with the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation">SetTokenInformation</a> function to set the default DACL.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation">SetTokenInformation</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_control">TOKEN_CONTROL</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>



<a href="/windows/desktop/api/winnt/ne-winnt-token_information_class">TOKEN_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_owner">TOKEN_OWNER</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_primary_group">TOKEN_PRIMARY_GROUP</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_source">TOKEN_SOURCE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_statistics">TOKEN_STATISTICS</a>



<a href="/windows/desktop/api/winnt/ne-winnt-token_type">TOKEN_TYPE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_user">TOKEN_USER</a>