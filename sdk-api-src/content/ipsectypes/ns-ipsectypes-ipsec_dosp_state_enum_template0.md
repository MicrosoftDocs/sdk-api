---
UID: NS:ipsectypes.IPSEC_DOSP_STATE_ENUM_TEMPLATE0_
title: IPSEC_DOSP_STATE_ENUM_TEMPLATE0 (ipsectypes.h)
description: The IPSEC_DOSP_STATE_ENUM_TEMPLATE0 structure.
helpviewer_keywords: ["IPSEC_DOSP_STATE_ENUM_TEMPLATE0","IPSEC_DOSP_STATE_ENUM_TEMPLATE0 structure [Filtering]","fwp.ipsec_dosp_state_enum_template0","ipsectypes/IPSEC_DOSP_STATE_ENUM_TEMPLATE0"]
old-location: fwp\ipsec_dosp_state_enum_template0.htm
tech.root: fwp
ms.assetid: bfc34949-dd80-4fcd-8147-2fed62bce387
ms.date: 12/05/2018
ms.keywords: IPSEC_DOSP_STATE_ENUM_TEMPLATE0, IPSEC_DOSP_STATE_ENUM_TEMPLATE0 structure [Filtering], fwp.ipsec_dosp_state_enum_template0, ipsectypes/IPSEC_DOSP_STATE_ENUM_TEMPLATE0
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: IPSEC_DOSP_STATE_ENUM_TEMPLATE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_DOSP_STATE_ENUM_TEMPLATE0_
 - ipsectypes/IPSEC_DOSP_STATE_ENUM_TEMPLATE0_
 - IPSEC_DOSP_STATE_ENUM_TEMPLATE0
 - ipsectypes/IPSEC_DOSP_STATE_ENUM_TEMPLATE0
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
 - IPSEC_DOSP_STATE_ENUM_TEMPLATE0
---

# IPSEC_DOSP_STATE_ENUM_TEMPLATE0 structure


## -description

The <b>IPSEC_DOSP_STATE_ENUM_TEMPLATE0</b> structure is used to enumerate IPsec DoS Protection state entries.

## -struct-fields

### -field publicV6AddrMask

An [FWP_V6_ADDR_AND_MASK](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_v6_addr_and_mask) structure that specifies the public IPv6 address.

### -field internalV6AddrMask

An [FWP_V6_ADDR_AND_MASK](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_v6_addr_and_mask) structure that specifies the internal IPv6 address.

## -remarks

<b>IPSEC_DOSP_STATE_ENUM_TEMPLATE0</b> is a specific implementation of IPSEC_DOSP_STATE_ENUM_TEMPLATE. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWP_V6_ADDR_AND_MASK](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_v6_addr_and_mask)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>