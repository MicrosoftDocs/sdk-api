---
UID: NC:ntsecpkg.LSA_GET_CLIENT_INFO
title: LSA_GET_CLIENT_INFO (ntsecpkg.h)
description: The GetClientInfo function gets information about the client process, such as thread and process ID, and flags indicating the client's state and privileges.
helpviewer_keywords: ["GetClientInfo","GetClientInfo callback function [Security]","LSA_GET_CLIENT_INFO","LSA_GET_CLIENT_INFO callback","_ssp_getclientinfo","ntsecpkg/GetClientInfo","security.getclientinfo"]
old-location: security\getclientinfo.htm
tech.root: security
ms.assetid: 3669f2e2-da70-4195-bdd0-f8415d97ae99
ms.date: 12/05/2018
ms.keywords: GetClientInfo, GetClientInfo callback function [Security], LSA_GET_CLIENT_INFO, LSA_GET_CLIENT_INFO callback, _ssp_getclientinfo, ntsecpkg/GetClientInfo, security.getclientinfo
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
 - LSA_GET_CLIENT_INFO
 - ntsecpkg/LSA_GET_CLIENT_INFO
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
 - GetClientInfo
---

# LSA_GET_CLIENT_INFO callback function


## -description

The <b>GetClientInfo</b> function gets information about the client process, such as thread and process ID, and flags indicating the client's state and privileges.

## -parameters

### -param ClientInfo [out]

Pointer to a 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_client_info">SECPKG_CLIENT_INFO</a> structure that receives information about the client.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code indicating the reason it failed.

## -remarks

A pointer to the <b>GetClientInfo</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>