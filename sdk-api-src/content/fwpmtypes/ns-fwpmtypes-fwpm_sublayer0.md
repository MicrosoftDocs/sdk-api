---
UID: NS:fwpmtypes.FWPM_SUBLAYER0_
title: FWPM_SUBLAYER0 (fwpmtypes.h)
description: Stores the state associated with a sublayer.
helpviewer_keywords: ["FWPM_SUBLAYER0","FWPM_SUBLAYER0 structure [Filtering]","FWPM_SUBLAYER_FLAG_PERSISTENT","fwp.fwpm_sublayer0_struct","fwpmtypes/FWPM_SUBLAYER0"]
old-location: fwp\fwpm_sublayer0_struct.htm
tech.root: fwp
ms.assetid: ce689b1d-1f5c-4dde-96cd-9001de3827aa
ms.date: 12/05/2018
ms.keywords: FWPM_SUBLAYER0, FWPM_SUBLAYER0 structure [Filtering], FWPM_SUBLAYER_FLAG_PERSISTENT, fwp.fwpm_sublayer0_struct, fwpmtypes/FWPM_SUBLAYER0
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
req.typenames: FWPM_SUBLAYER0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_SUBLAYER0_
 - fwpmtypes/FWPM_SUBLAYER0_
 - FWPM_SUBLAYER0
 - fwpmtypes/FWPM_SUBLAYER0
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
 - FWPM_SUBLAYER0
---

# FWPM_SUBLAYER0 structure


## -description

The <b>FWPM_SUBLAYER0</b> structure stores the state associated with a sublayer.

## -struct-fields

### -field subLayerKey

Uniquely identifies the sublayer. See <a href="/windows/desktop/FWP/management-filtering-sublayer-identifiers">Filtering Sublayer Identifiers</a> for a list of built-in sublayers.

If the GUID is zero-initialized in the call to <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsublayeradd0">FwpmSubLayerAdd0</a>, the Base Filtering Engine (BFE) will generate one.

### -field displayData

Allows sublayers to be annotated in human-readable form.   The [FWPM_DISPLAY_DATA0](/windows/desktop/api/fwptypes/ns-fwptypes-fwpm_display_data0) structure is required.

### -field flags

Possible values:

<table>
<tr>
<th>Sublayer flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWPM_SUBLAYER_FLAG_PERSISTENT"></a><a id="fwpm_sublayer_flag_persistent"></a><dl>
<dt><b>FWPM_SUBLAYER_FLAG_PERSISTENT</b></dt>
</dl>
</td>
<td width="60%">
Causes sublayer to be persistent, surviving across BFE stop/start.

</td>
</tr>
</table>

### -field providerKey

Uniquely identifies the provider that manages this sublayer.

### -field providerData

An [FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob) structure that contains optional provider-specific data that allows providers to store additional context info with the object.

### -field weight

Weight of the sublayer. 

Higher-weighted sublayers are invoked first.

## -remarks

<b>FWPM_SUBLAYER0</b> is a specific implementation of FWPM_SUBLAYER. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>