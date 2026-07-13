---
UID: NS:iketypes.IKEEXT_SA_ENUM_TEMPLATE0_
title: IKEEXT_SA_ENUM_TEMPLATE0 (iketypes.h)
description: Is an enumeration template used for enumerating IKE/AuthIP security associations (SAs).
helpviewer_keywords: ["IKEEXT_SA_ENUM_TEMPLATE0","IKEEXT_SA_ENUM_TEMPLATE0 structure [Filtering]","fwp.ikeext_sa_enum_template0","iketypes/IKEEXT_SA_ENUM_TEMPLATE0"]
old-location: fwp\ikeext_sa_enum_template0.htm
tech.root: fwp
ms.assetid: 69bb80de-e512-4fbd-a62f-40bb211e6b26
ms.date: 12/05/2018
ms.keywords: IKEEXT_SA_ENUM_TEMPLATE0, IKEEXT_SA_ENUM_TEMPLATE0 structure [Filtering], fwp.ikeext_sa_enum_template0, iketypes/IKEEXT_SA_ENUM_TEMPLATE0
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IKEEXT_SA_ENUM_TEMPLATE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_SA_ENUM_TEMPLATE0_
 - iketypes/IKEEXT_SA_ENUM_TEMPLATE0_
 - IKEEXT_SA_ENUM_TEMPLATE0
 - iketypes/IKEEXT_SA_ENUM_TEMPLATE0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_SA_ENUM_TEMPLATE0
---

# IKEEXT_SA_ENUM_TEMPLATE0 structure


## -description

The <b>IKEEXT_SA_ENUM_TEMPLATE0</b> structure is an enumeration template used for enumerating IKE/AuthIP security associations (SAs).

## -struct-fields

### -field localSubNet

Matches SAs whose local address is on the specified subnet. Must be of one of the following types.

<ul>
<li>FWP_UINT32</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
<li>FWP_V4_ADDR_MASK</li>
<li>FWP_V6_ADDR_MASK</li>
</ul>
See [FWP_CONDITION_VALUE0](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_condition_value0) for more information.

### -field remoteSubNet

Matches SAs whose remote address is on the specified subnet. Must be of one of the following types.

<ul>
<li>FWP_UINT32</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
<li>FWP_V4_ADDR_MASK</li>
<li>FWP_V6_ADDR_MASK</li>
</ul>
See [FWP_CONDITION_VALUE0](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_condition_value0) for more information.

### -field localMainModeCertHash

Matches SAs with a matching local main mode SHA thumbprint.  If none exist, this member will have a length of zero.

See [FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob) for more information.

## -remarks

<b>IKEEXT_SA_ENUM_TEMPLATE0</b> is a specific implementation of IKEEXT_SA_ENUM_TEMPLATE. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>