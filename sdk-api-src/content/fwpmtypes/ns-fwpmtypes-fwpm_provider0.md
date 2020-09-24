---
UID: NS:fwpmtypes.FWPM_PROVIDER0_
title: FWPM_PROVIDER0 (fwpmtypes.h)
description: Stores the state associated with a policy provider.
helpviewer_keywords: ["FWPM_PROVIDER0","FWPM_PROVIDER0 structure [Filtering]","FWPM_PROVIDER_FLAG_DISABLED","FWPM_PROVIDER_FLAG_PERSISTENT","fwp.fwpm_provider0_struct","fwpmtypes/FWPM_PROVIDER0"]
old-location: fwp\fwpm_provider0_struct.htm
tech.root: fwp
ms.assetid: 692714fd-14f1-4f8b-a033-1f30b6d0b95a
ms.date: 12/05/2018
ms.keywords: FWPM_PROVIDER0, FWPM_PROVIDER0 structure [Filtering], FWPM_PROVIDER_FLAG_DISABLED, FWPM_PROVIDER_FLAG_PERSISTENT, fwp.fwpm_provider0_struct, fwpmtypes/FWPM_PROVIDER0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: FWPM_PROVIDER0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_PROVIDER0_
 - fwpmtypes/FWPM_PROVIDER0_
 - FWPM_PROVIDER0
 - fwpmtypes/FWPM_PROVIDER0
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
 - FWPM_PROVIDER0
---

# FWPM_PROVIDER0 structure


## -description

The <b>FWPM_PROVIDER0</b> structure stores the state associated with a policy provider.

## -struct-fields

### -field providerKey

Uniquely identifies the provider. 

If the GUID is zero-initialized in the
   call to Add, Base Filtering Engine (BFE) will generate one.

### -field displayData

Allows providers to be annotated in a human-readable form.  The [FWPM_DISPLAY_DATA0](/windows/desktop/api/fwptypes/ns-fwptypes-fwpm_display_data0) structure is required.

### -field flags

Bit flags that indicate information about the persistence of the provider.

<table>
<tr>
<th>Provider flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWPM_PROVIDER_FLAG_PERSISTENT"></a><a id="fwpm_provider_flag_persistent"></a><dl>
<dt><b>FWPM_PROVIDER_FLAG_PERSISTENT</b></dt>
</dl>
</td>
<td width="60%">
Provider is persistent.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_PROVIDER_FLAG_DISABLED"></a><a id="fwpm_provider_flag_disabled"></a><dl>
<dt><b>FWPM_PROVIDER_FLAG_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
Provider's filters were disabled when the BFE started because the provider has no associated Windows service name, or because the associated service was not set to auto-start. 

<div class="alert"><b>Note</b>  This flag cannot be set when adding new providers. It can only be returned by BFE when getting or enumerating providers.</div>
<div> </div>
</td>
</tr>
</table>

### -field providerData

An [FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob) structure that contains optional provider-specific data that allows providers to store additional context info with the object.

### -field serviceName

Optional name of the Windows service hosting the provider. This allows
   BFE to detect that a provider has been disabled.

## -remarks

<b>FWPM_PROVIDER0</b> is a specific implementation of FWPM_PROVIDER. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_DISPLAY_DATA0](/windows/desktop/api/fwptypes/ns-fwptypes-fwpm_display_data0)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>