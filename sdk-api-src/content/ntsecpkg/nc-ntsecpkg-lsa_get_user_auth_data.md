---
UID: NC:ntsecpkg.LSA_GET_USER_AUTH_DATA
title: LSA_GET_USER_AUTH_DATA (ntsecpkg.h)
description: The GetUserAuthData function returns the authorization data for the user in a single buffer.
helpviewer_keywords: ["GetUserAuthData","GetUserAuthData callback function [Security]","LSA_GET_USER_AUTH_DATA","LSA_GET_USER_AUTH_DATA callback","_ssp_getuserauthdata","ntsecpkg/GetUserAuthData","security.getuserauthdata"]
old-location: security\getuserauthdata.htm
tech.root: security
ms.assetid: 2436eaee-1f32-4e32-9a98-74968ad9b58e
ms.date: 12/05/2018
ms.keywords: GetUserAuthData, GetUserAuthData callback function [Security], LSA_GET_USER_AUTH_DATA, LSA_GET_USER_AUTH_DATA callback, _ssp_getuserauthdata, ntsecpkg/GetUserAuthData, security.getuserauthdata
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
 - LSA_GET_USER_AUTH_DATA
 - ntsecpkg/LSA_GET_USER_AUTH_DATA
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
 - GetUserAuthData
---

# LSA_GET_USER_AUTH_DATA callback function


## -description

The <b>GetUserAuthData</b> function returns the authorization data for the user in a single buffer.

## -parameters

### -param UserHandle [in]

A handle to the user account. This handle is returned by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_open_sam_user">OpenSamUser</a> function.

### -param UserAuthData [out]

Pointer that receives the consolidated authorization data. When you have finished using the authorization data, free the memory by calling the <a href="/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap">FreeLsaHeap</a> function.

### -param UserAuthDataSize [out]

Pointer that receives the size of the authorization data.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code indicating the reason it failed.

## -remarks

The authorization data returned by the <b>GetUserAuthData</b> function can be passed to the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_convert_auth_data_to_token">ConvertAuthDataToToken</a> function.

A pointer to the <b>GetUserAuthData</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_convert_auth_data_to_token">ConvertAuthDataToToken</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_open_sam_user">OpenSamUser</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>
