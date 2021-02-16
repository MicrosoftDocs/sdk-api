---
UID: NS:winnt._TOKEN_CONTROL
title: TOKEN_CONTROL (winnt.h)
description: Contains information that identifies an access token.
helpviewer_keywords: ["*PTOKEN_CONTROL","PTOKEN_CONTROL","PTOKEN_CONTROL structure pointer [Security]","TOKEN_CONTROL","TOKEN_CONTROL structure [Security]","_TOKEN_CONTROL","_win32_token_control_str","security.token_control","winnt/PTOKEN_CONTROL","winnt/TOKEN_CONTROL"]
old-location: security\token_control.htm
tech.root: security
ms.assetid: b87c942b-8e58-471d-8cdf-e46cdac647c4
ms.date: 12/05/2018
ms.keywords: '*PTOKEN_CONTROL, PTOKEN_CONTROL, PTOKEN_CONTROL structure pointer [Security], TOKEN_CONTROL, TOKEN_CONTROL structure [Security], _TOKEN_CONTROL, _win32_token_control_str, security.token_control, winnt/PTOKEN_CONTROL, winnt/TOKEN_CONTROL'
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
req.typenames: TOKEN_CONTROL, *PTOKEN_CONTROL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TOKEN_CONTROL
 - winnt/_TOKEN_CONTROL
 - PTOKEN_CONTROL
 - winnt/PTOKEN_CONTROL
 - TOKEN_CONTROL
 - winnt/TOKEN_CONTROL
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
 - TOKEN_CONTROL
---

# TOKEN_CONTROL structure


## -description

The <b>TOKEN_CONTROL</b> structure contains information that identifies an <a href="/windows/desktop/SecGloss/a-gly">access token</a>.

## -struct-fields

### -field TokenId

Specifies a <a href="/windows/desktop/SecGloss/l-gly">locally unique identifier</a> (LUID) identifying this instance of the token object.

### -field AuthenticationId

Specifies an LUID assigned to the <a href="/windows/desktop/SecGloss/s-gly">session</a> this token represents. There can be many tokens representing a single <a href="/windows/desktop/SecGloss/l-gly">logon session</a>.

### -field ModifiedId

Specifies an LUID that changes each time the token is modified. An application can use this value as a test of whether a <a href="/windows/desktop/SecGloss/s-gly">security context</a> has changed since it was last used.

### -field TokenSource

Specifies a <a href="/windows/desktop/api/winnt/ns-winnt-token_source">TOKEN_SOURCE</a> structure identifying the agency that issued the token. This information is used in audit trails.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_default_dacl">TOKEN_DEFAULT_DACL</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>



<a href="/windows/desktop/api/winnt/ne-winnt-token_information_class">TOKEN_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_owner">TOKEN_OWNER</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_primary_group">TOKEN_PRIMARY_GROUP</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_source">TOKEN_SOURCE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_statistics">TOKEN_STATISTICS</a>



<a href="/windows/desktop/api/winnt/ne-winnt-token_type">TOKEN_TYPE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_user">TOKEN_USER</a>