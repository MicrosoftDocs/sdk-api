---
UID: NS:ipsectypes.IPSEC_SA_AUTH_INFORMATION0_
title: IPSEC_SA_AUTH_INFORMATION0 (ipsectypes.h)
description: Stores information about the authentication algorithm of an IPsec security association (SA).
helpviewer_keywords: ["IPSEC_SA_AUTH_INFORMATION0","IPSEC_SA_AUTH_INFORMATION0 structure [Filtering]","fwp.ipsec_sa_auth_information0_struct","ipsectypes/IPSEC_SA_AUTH_INFORMATION0"]
old-location: fwp\ipsec_sa_auth_information0_struct.htm
tech.root: fwp
ms.assetid: 54a03edd-94cb-478a-a647-473872408701
ms.date: 12/05/2018
ms.keywords: IPSEC_SA_AUTH_INFORMATION0, IPSEC_SA_AUTH_INFORMATION0 structure [Filtering], fwp.ipsec_sa_auth_information0_struct, ipsectypes/IPSEC_SA_AUTH_INFORMATION0
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
req.typenames: IPSEC_SA_AUTH_INFORMATION0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_SA_AUTH_INFORMATION0_
 - ipsectypes/IPSEC_SA_AUTH_INFORMATION0_
 - IPSEC_SA_AUTH_INFORMATION0
 - ipsectypes/IPSEC_SA_AUTH_INFORMATION0
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
 - IPSEC_SA_AUTH_INFORMATION0
---

# IPSEC_SA_AUTH_INFORMATION0 structure


## -description

The <b>IPSEC_SA_AUTH_INFORMATION0</b> structure stores information about the authentication algorithm of an IPsec security association (SA).

## -struct-fields

### -field authTransform

Authentication algorithm details as specified by [IPSEC_AUTH_TRANSFORM0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_auth_transform0).

### -field authKey

Key used for the authentication algorithm stored in a [FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob) structure.

## -remarks

<b>IPSEC_SA_AUTH_INFORMATION0</b> is a specific implementation of IPSEC_SA_AUTH_INFORMATION. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)



[IPSEC_AUTH_TRANSFORM0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_auth_transform0)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>