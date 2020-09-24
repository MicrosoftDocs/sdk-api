---
UID: NS:fwpmtypes.FWPM_CLASSIFY_OPTION0_
title: FWPM_CLASSIFY_OPTION0 (fwpmtypes.h)
description: The FWPM_CLASSIFY_OPTION0 structure.
helpviewer_keywords: ["FWPM_CLASSIFY_OPTION0","FWPM_CLASSIFY_OPTION0 structure [Filtering]","fwp.fwpm_classify_option0","fwpmtypes/FWPM_CLASSIFY_OPTION0"]
old-location: fwp\fwpm_classify_option0.htm
tech.root: fwp
ms.assetid: 11f2f873-d27e-411c-ba5b-a93134e1f027
ms.date: 12/05/2018
ms.keywords: FWPM_CLASSIFY_OPTION0, FWPM_CLASSIFY_OPTION0 structure [Filtering], fwp.fwpm_classify_option0, fwpmtypes/FWPM_CLASSIFY_OPTION0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWPM_CLASSIFY_OPTION0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_CLASSIFY_OPTION0_
 - fwpmtypes/FWPM_CLASSIFY_OPTION0_
 - FWPM_CLASSIFY_OPTION0
 - fwpmtypes/FWPM_CLASSIFY_OPTION0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_CLASSIFY_OPTION0
---

# FWPM_CLASSIFY_OPTION0 structure


## -description

The <b>FWPM_CLASSIFY_OPTION0</b> structure is used to define unicast and multicast timeout options and data.

## -struct-fields

### -field type

An [FWP_CLASSIFY_OPTION_TYPE](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_classify_option_type) value.

### -field value

An [FWP_VALUE0](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_value0) structure.

## -remarks

The following table lists possible values for the members of a <b>FWPM_CLASSIFY_OPTION0</b> structure.

<table>
<tr>
<th><b>type</b></th>
<th><b>value</b></th>
</tr>
<tr>
<td>FWP_CLASSIFY_OPTION_MULTICAST_STATE</td>
<td>
<ul>
<li>FWP_OPTION_VALUE_ALLOW_MULTICAST_STATE Allow link-local multicast state creation on outbound traffic

</li>
<li>FWP_OPTION_VALUE_DENY_MULTICAST_STATE  Do not allow link-local multicast state creation on outbound traffic

</li>
<li>FWP_OPTION_VALUE_ALLOW_GLOBAL_MULTICAST_STATE Allow global multicast state creation on outbound traffic

</li>
</ul>
</td>
</tr>
<tr>
<td>FWP_CLASSIFY_OPTION_LOOSE_SOURCE_MAPPING</td>
<td>
<ul>
<li>FWP_OPTION_VALUE_ENABLE_LOOSE_SOURCE Enable loose source mapping

</li>
<li>FWP_OPTION_VALUE_DISABLE_LOOSE_SOURCE Disable loose source mapping

</li>
</ul>
</td>
</tr>
<tr>
<td>FWP_CLASSIFY_OPTION_UNICAST_LIFETIME</td>
<td>
<ul>
<li>Any FWP_UINT32</li>
</ul>
</td>
</tr>
<tr>
<td>FWP_CLASSIFY_OPTION_MCAST_BCAST_LIFETIME</td>
<td>
<ul>
<li>Any FWP_UINT32</li>
</ul>
</td>
</tr>
</table>
 

<b>FWPM_CLASSIFY_OPTION0</b> is a specific implementation of FWPM_CLASSIFY_OPTION. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_CLASSIFY_OPTIONS0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_classify_options0)



[FWP_CLASSIFY_OPTION_TYPE](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_classify_option_type)



[FWP_VALUE0](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_value0)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>