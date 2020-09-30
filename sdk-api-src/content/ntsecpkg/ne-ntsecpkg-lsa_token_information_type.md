---
UID: NE:ntsecpkg._LSA_TOKEN_INFORMATION_TYPE
title: LSA_TOKEN_INFORMATION_TYPE (ntsecpkg.h)
description: Specifies the levels of information that can be included in a logon token.
helpviewer_keywords: ["*PLSA_TOKEN_INFORMATION_TYPE","LSA_TOKEN_INFORMATION_TYPE","LSA_TOKEN_INFORMATION_TYPE enumeration [Security]","LsaTokenInformationNull","LsaTokenInformationV1","PLSA_TOKEN_INFORMATION_TYPE","PLSA_TOKEN_INFORMATION_TYPE enumeration pointer [Security]","_lsa_lsa_token_information_type","ntsecpkg/LSA_TOKEN_INFORMATION_TYPE","ntsecpkg/LsaTokenInformationNull","ntsecpkg/LsaTokenInformationV1","ntsecpkg/PLSA_TOKEN_INFORMATION_TYPE","security.lsa_token_information_type"]
old-location: security\lsa_token_information_type.htm
tech.root: security
ms.assetid: c8bf5b8d-6cb1-469d-a451-6cceafda24cf
ms.date: 12/05/2018
ms.keywords: '*PLSA_TOKEN_INFORMATION_TYPE, LSA_TOKEN_INFORMATION_TYPE, LSA_TOKEN_INFORMATION_TYPE enumeration [Security], LsaTokenInformationNull, LsaTokenInformationV1, PLSA_TOKEN_INFORMATION_TYPE, PLSA_TOKEN_INFORMATION_TYPE enumeration pointer [Security], _lsa_lsa_token_information_type, ntsecpkg/LSA_TOKEN_INFORMATION_TYPE, ntsecpkg/LsaTokenInformationNull, ntsecpkg/LsaTokenInformationV1, ntsecpkg/PLSA_TOKEN_INFORMATION_TYPE, security.lsa_token_information_type'
req.header: ntsecpkg.h
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
req.typenames: LSA_TOKEN_INFORMATION_TYPE, *PLSA_TOKEN_INFORMATION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LSA_TOKEN_INFORMATION_TYPE
 - ntsecpkg/_LSA_TOKEN_INFORMATION_TYPE
 - PLSA_TOKEN_INFORMATION_TYPE
 - ntsecpkg/PLSA_TOKEN_INFORMATION_TYPE
 - LSA_TOKEN_INFORMATION_TYPE
 - ntsecpkg/LSA_TOKEN_INFORMATION_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - LSA_TOKEN_INFORMATION_TYPE
---

# LSA_TOKEN_INFORMATION_TYPE enumeration


## -description

The <b>LSA_TOKEN_INFORMATION_TYPE</b> enumeration specifies the levels of information that can be included in a logon token.

When the LSA calls either 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user">LsaApLogonUser</a>, 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user_ex">LsaApLogonUserEx</a>, or 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user_ex2">LsaApLogonUserEx2</a> the <a href="/windows/desktop/SecGloss/a-gly">authentication package</a> is expected to return one of the following enumeration values to indicate the type of token information structure returned.

## -enum-fields

### -field LsaTokenInformationNull

The token information is stored in an 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_token_information_null">LSA_TOKEN_INFORMATION_NULL</a> structure. 




This token information type is used for anonymous logons or <b>null</b> sessions, where a token is needed but the client's identity is unknown.

For example, a non-authenticated network circuit (such as a domain controller's <b>null</b> session) can be given <b>NULL</b> information. In this case, an anonymous token is generated for the logon. An anonymous token does not permit access to protected system resources, but does allow access to unprotected system resources.

### -field LsaTokenInformationV1

The token information is stored in a 
<a href="/previous-versions/windows/desktop/legacy/aa378721(v=vs.85)">LSA_TOKEN_INFORMATION_V1</a> structure. This structure contains information that an authentication package can place in a Version 1 Windows token object. A Version 1 Windows token object stores all the information needed to build a token and is used in most logon cases. The LSA creates the token object, and returns a handle to that token object to the caller of 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a>.

### -field LsaTokenInformationV2

### -field LsaTokenInformationV3