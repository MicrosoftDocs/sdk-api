---
UID: NS:winnt._TOKEN_USER
title: TOKEN_USER (winnt.h)
description: Identifies the user associated with an access token.
old-location: security\token_user.htm
tech.root: SecAuthZ
ms.assetid: 5dd8172d-7b1a-4cc0-b667-5fe91d278393
ms.date: 12/05/2018
ms.keywords: '*PTOKEN_USER, PTOKEN_USER, PTOKEN_USER structure pointer [Security], TOKEN_USER, TOKEN_USER structure [Security], _TOKEN_USER, _win32_token_user_str, security.token_user, winnt/PTOKEN_USER, winnt/TOKEN_USER'
ms.topic: struct
f1_keywords:
- winnt/TOKEN_USER
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Winnt.h
api_name:
- TOKEN_USER
targetos: Windows
req.typenames: TOKEN_USER, *PTOKEN_USER
req.redist: 
ms.custom: 19H1
---

# TOKEN_USER structure


## -description


The <b>TOKEN_USER</b> structure identifies the user associated with an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">access token</a>.


## -struct-fields




### -field User

Specifies a
						<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-sid_and_attributes">SID_AND_ATTRIBUTES</a> structure representing the user associated with the access token. There are currently no attributes defined for user <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs).


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-sid_and_attributes">SID_AND_ATTRIBUTES</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-token_control">TOKEN_CONTROL</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-token_default_dacl">TOKEN_DEFAULT_DACL</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ne-winnt-token_information_class">TOKEN_INFORMATION_CLASS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-token_owner">TOKEN_OWNER</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-token_primary_group">TOKEN_PRIMARY_GROUP</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-token_source">TOKEN_SOURCE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-token_statistics">TOKEN_STATISTICS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ne-winnt-token_type">TOKEN_TYPE</a>
 

 

