---
UID: NC:ntsecpkg.LSA_EXPAND_AUTH_DATA_FOR_DOMAIN
title: LSA_EXPAND_AUTH_DATA_FOR_DOMAIN (ntsecpkg.h)
description: Expands the domain groups in the specified user authentication data.
helpviewer_keywords: ["ExpandAuthDataForDomain","ExpandAuthDataForDomain callback function [Security]","LSA_EXPAND_AUTH_DATA_FOR_DOMAIN","LSA_EXPAND_AUTH_DATA_FOR_DOMAIN callback","ntsecpkg/ExpandAuthDataForDomain","security.expandauthdatafordomain"]
old-location: security\expandauthdatafordomain.htm
tech.root: security
ms.assetid: 965d8575-a05b-45d8-8718-4004f1d22ca5
ms.date: 12/05/2018
ms.keywords: ExpandAuthDataForDomain, ExpandAuthDataForDomain callback function [Security], LSA_EXPAND_AUTH_DATA_FOR_DOMAIN, LSA_EXPAND_AUTH_DATA_FOR_DOMAIN callback, ntsecpkg/ExpandAuthDataForDomain, security.expandauthdatafordomain
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
 - LSA_EXPAND_AUTH_DATA_FOR_DOMAIN
 - ntsecpkg/LSA_EXPAND_AUTH_DATA_FOR_DOMAIN
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
 - ExpandAuthDataForDomain
---

# LSA_EXPAND_AUTH_DATA_FOR_DOMAIN callback function


## -description

Expands the domain groups in the specified user authentication data.

## -parameters

### -param UserAuthData [in]

A pointer to the user authentication data to expand.

### -param UserAuthDataSize [in]

The size, in bytes, of the <i>UserAuthData</i> buffer.

### -param Reserved [in]

Reserved. This parameter must be set to <b>NULL.</b>

### -param ExpandedAuthData [out]

A pointer to the expanded authentication data.

### -param ExpandedAuthDataSize [out]

A pointer to the size, in bytes, of the <i>ExpandedAuthData</i> buffer.

## -returns

If the function succeeds, return STATUS_SUCCESS, or an informational status code.

If the function fails, return an NTSTATUS error code that indicates the reason it failed.

## -remarks

A pointer to the <b>ExpandAuthDataForDomain</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>
