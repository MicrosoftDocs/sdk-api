---
UID: NC:ntsecpkg.LSA_OPEN_TOKEN_BY_LOGON_ID
title: LSA_OPEN_TOKEN_BY_LOGON_ID (ntsecpkg.h)
description: Opens the user access token associated with the specified user logon.
helpviewer_keywords: ["LSA_OPEN_TOKEN_BY_LOGON_ID","LSA_OPEN_TOKEN_BY_LOGON_ID callback","OpenTokenByLogonId","OpenTokenByLogonId callback function [Security]","ntsecpkg/OpenTokenByLogonId","security.opentokenbylogonid"]
old-location: security\opentokenbylogonid.htm
tech.root: security
ms.assetid: 3cd3e4fe-7548-44f9-ab04-01b30bdf3bd9
ms.date: 12/05/2018
ms.keywords: LSA_OPEN_TOKEN_BY_LOGON_ID, LSA_OPEN_TOKEN_BY_LOGON_ID callback, OpenTokenByLogonId, OpenTokenByLogonId callback function [Security], ntsecpkg/OpenTokenByLogonId, security.opentokenbylogonid
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LSA_OPEN_TOKEN_BY_LOGON_ID
 - ntsecpkg/LSA_OPEN_TOKEN_BY_LOGON_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - OpenTokenByLogonId
---

# LSA_OPEN_TOKEN_BY_LOGON_ID callback function


## -description

Opens the user access token associated with the specified user logon.

## -parameters

### -param LogonId [in]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a> structure that identifies the user for which to open the access token.

### -param RetTokenHandle [out]

A pointer to the handle to the token this function opens.

## -returns

If the function succeeds, return STATUS_SUCCESS, or an informational status code.

If the function fails, return an NTSTATUS error code that indicates the reason it failed.

## -remarks

A pointer to the <b>OpenTokenByLogonId</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>
