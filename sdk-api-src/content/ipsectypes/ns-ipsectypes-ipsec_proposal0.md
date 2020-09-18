---
UID: NS:ipsectypes.IPSEC_PROPOSAL0_
title: IPSEC_PROPOSAL0 (ipsectypes.h)
description: Used to store an IPsec quick mode proposal.
helpviewer_keywords: ["IPSEC_PROPOSAL0","IPSEC_PROPOSAL0 structure [Filtering]","fwp.ipsec_proposal0_struct","ipsectypes/IPSEC_PROPOSAL0"]
old-location: fwp\ipsec_proposal0_struct.htm
tech.root: fwp
ms.assetid: bc551733-dbba-4d66-8054-fbf4bbfa28b5
ms.date: 12/05/2018
ms.keywords: IPSEC_PROPOSAL0, IPSEC_PROPOSAL0 structure [Filtering], fwp.ipsec_proposal0_struct, ipsectypes/IPSEC_PROPOSAL0
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
req.typenames: IPSEC_PROPOSAL0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_PROPOSAL0_
 - ipsectypes/IPSEC_PROPOSAL0_
 - IPSEC_PROPOSAL0
 - ipsectypes/IPSEC_PROPOSAL0
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
 - IPSEC_PROPOSAL0
---

# IPSEC_PROPOSAL0 structure


## -description

The <b>IPSEC_PROPOSAL0</b> structure is used to store an IPsec quick mode proposal.

## -struct-fields

### -field lifetime

Lifetime of the IPsec security association (SA) as specified by [IPSEC_SA_LIFETIME0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_lifetime0). Cannot be zero.

### -field numSaTransforms

Number of IPsec SA transforms. The only possible values are 1 and 2. Use 2 only when specifying AH plus ESP transforms.

### -field saTransforms

Array of IPsec SA transforms as specified by [IPSEC_SA_TRANSFORM0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_transform0).

### -field pfsGroup

Perfect forward secrecy (PFS) group of the IPsec SA as specified by [IPSEC_PFS_GROUP](/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_pfs_group).

## -remarks

The proposal describes the
various parameters of the IPsec SA that is potentially generated from this
proposal.

<b>IPSEC_PROPOSAL0</b> is a specific implementation of IPSEC_PROPOSAL. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[IPSEC_PFS_GROUP](/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_pfs_group)



[IPSEC_SA_LIFETIME0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_lifetime0)



[IPSEC_SA_TRANSFORM0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_transform0)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>