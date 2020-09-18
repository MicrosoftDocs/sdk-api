---
UID: NS:ipsectypes.IPSEC_SA_CONTEXT_ENUM_TEMPLATE0_
title: IPSEC_SA_CONTEXT_ENUM_TEMPLATE0 (ipsectypes.h)
description: Enumeration template used to enumerate security association (SA) contexts.
helpviewer_keywords: ["IPSEC_SA_CONTEXT_ENUM_TEMPLATE0","IPSEC_SA_CONTEXT_ENUM_TEMPLATE0 structure [Filtering]","fwp.ipsec_sa_context_enum_template0","ipsectypes/IPSEC_SA_CONTEXT_ENUM_TEMPLATE0"]
old-location: fwp\ipsec_sa_context_enum_template0.htm
tech.root: fwp
ms.assetid: 2e099545-4075-4ea0-9035-53ce334decc4
ms.date: 12/05/2018
ms.keywords: IPSEC_SA_CONTEXT_ENUM_TEMPLATE0, IPSEC_SA_CONTEXT_ENUM_TEMPLATE0 structure [Filtering], fwp.ipsec_sa_context_enum_template0, ipsectypes/IPSEC_SA_CONTEXT_ENUM_TEMPLATE0
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
req.typenames: IPSEC_SA_CONTEXT_ENUM_TEMPLATE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_SA_CONTEXT_ENUM_TEMPLATE0_
 - ipsectypes/IPSEC_SA_CONTEXT_ENUM_TEMPLATE0_
 - IPSEC_SA_CONTEXT_ENUM_TEMPLATE0
 - ipsectypes/IPSEC_SA_CONTEXT_ENUM_TEMPLATE0
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
 - IPSEC_SA_CONTEXT_ENUM_TEMPLATE0
---

# IPSEC_SA_CONTEXT_ENUM_TEMPLATE0 structure


## -description

The <b>IPSEC_SA_CONTEXT_ENUM_TEMPLATE0</b>	structure is an enumeration template used to enumerate security association (SA) contexts.

## -struct-fields

### -field localSubNet

An [FWP_CONDITION_VALUE0](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_condition_value0) structure that specifies a subnet from which SA contexts that contain a local address will be returned.  This member may be empty.

Acceptable type values for this member are: [FWP_V6_ADDR_AND_MASK](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_v6_addr_and_mask).

### -field remoteSubNet

An [FWP_CONDITION_VALUE0](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_condition_value0) structure that specifies a subnet from which SA contexts that contain a remote address will be returned.  This member may be empty.

Acceptable type values for this member are: [FWP_V6_ADDR_AND_MASK](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_v6_addr_and_mask).

## -remarks

<b>IPSEC_SA_CONTEXT_ENUM_TEMPLATE0</b> is a specific implementation of IPSEC_SA_CONTEXT_ENUM_TEMPLATE. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWP_CONDITION_VALUE0](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_condition_value0)