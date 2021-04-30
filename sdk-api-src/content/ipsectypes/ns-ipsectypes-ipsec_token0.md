---
UID: NS:ipsectypes.IPSEC_TOKEN0_
title: IPSEC_TOKEN0 (ipsectypes.h)
description: Various information about an IPsec-specific access token.
helpviewer_keywords: ["IPSEC_TOKEN0","IPSEC_TOKEN0 structure [Filtering]","fwp.ipsec_token0","ipsectypes/IPSEC_TOKEN0"]
old-location: fwp\ipsec_token0.htm
tech.root: fwp
ms.assetid: 12adf88e-05c7-4e08-bbf7-6da529387af1
ms.date: 12/05/2018
ms.keywords: IPSEC_TOKEN0, IPSEC_TOKEN0 structure [Filtering], fwp.ipsec_token0, ipsectypes/IPSEC_TOKEN0
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
req.typenames: IPSEC_TOKEN0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_TOKEN0_
 - ipsectypes/IPSEC_TOKEN0_
 - IPSEC_TOKEN0
 - ipsectypes/IPSEC_TOKEN0
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
 - IPSEC_TOKEN0
---

# IPSEC_TOKEN0 structure


## -description

The <b>IPSEC_TOKEN0</b> structure contains various information about an IPsec-specific access token.

## -struct-fields

### -field type

An [IPSEC_TOKEN_TYPE](/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_token_type) value that specifies the type of token.

### -field principal

An [IPSEC_TOKEN_PRINCIPAL](/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_token_principal) value that specifies the token principal.

### -field mode

An [IPSEC_TOKEN_MODE](/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_token_mode) value that indicates in which mode the token was obtained.

### -field token

Handle to the access token.  An <b>IPSEC_TOKEN_HANDLE</b> is of type <b>UINT64</b>.

## -remarks

<b>IPSEC_TOKEN0</b> is a specific implementation of IPSEC_TOKEN. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.