---
UID: NS:ipsectypes.IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0_
title: IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0 (ipsectypes.h)
description: Stores information about the authentication and encryption algorithms of an IPsec security association (SA).
helpviewer_keywords: ["IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0","IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0 structure [Filtering]","fwp.ipsec_sa_auth_and_cipher_information0_struct","ipsectypes/IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0"]
old-location: fwp\ipsec_sa_auth_and_cipher_information0_struct.htm
tech.root: fwp
ms.assetid: 0e213ba0-3993-41da-8ddd-5ecde7942a95
ms.date: 12/05/2018
ms.keywords: IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0, IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0 structure [Filtering], fwp.ipsec_sa_auth_and_cipher_information0_struct, ipsectypes/IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0_
 - ipsectypes/IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0_
 - IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0
 - ipsectypes/IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0
---

# IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0 structure


## -description

The <b>IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0</b> structure stores information about the authentication and encryption algorithms of an IPsec security association (SA).

## -struct-fields

### -field saCipherInformation

Encryption algorithm information as specified by [IPSEC_SA_CIPHER_INFORMATION0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_cipher_information0).

### -field saAuthInformation

Authentication algorithm information as specified by [IPSEC_SA_AUTH_INFORMATION0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_auth_information0).

## -remarks

<b>IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0</b> is a specific implementation of IPSEC_SA_AUTH_AND_CIPHER_INFORMATION. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[IPSEC_SA_AUTH_INFORMATION0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_auth_information0)



[IPSEC_SA_CIPHER_INFORMATION0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_cipher_information0)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>