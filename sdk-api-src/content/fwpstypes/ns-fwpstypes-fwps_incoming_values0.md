---
UID: NS:fwpstypes.FWPS_INCOMING_VALUES0_
title: FWPS_INCOMING_VALUES0 (fwpstypes.h)
description: The FWPS_INCOMING_VALUES0 structure defines data values that are passed by the filter engine to a callout's classifyFn callout function.Note  FWPS_INCOMING_VALUES0 is a specific version of FWPS_INCOMING_VALUES.
helpviewer_keywords: ["FWPS_INCOMING_VALUES0","FWPS_INCOMING_VALUES0 structure [Network Drivers Starting with Windows Vista]","fwpstypes/FWPS_INCOMING_VALUES0","netvista.fwps_incoming_values0","wfp_ref_3_struct_3_fwps_F-O_8a5ec685-98ff-49f2-9e78-72d409fece93.xml"]
old-location: netvista\fwps_incoming_values0.htm
tech.root: NetVista
ms.assetid: 62cec782-3d55-4bf0-a3a1-4eb2f11d5813
ms.date: 12/05/2018
ms.keywords: FWPS_INCOMING_VALUES0, FWPS_INCOMING_VALUES0 structure [Network Drivers Starting with Windows Vista], fwpstypes/FWPS_INCOMING_VALUES0, netvista.fwps_incoming_values0, wfp_ref_3_struct_3_fwps_F-O_8a5ec685-98ff-49f2-9e78-72d409fece93.xml
req.header: fwpstypes.h
req.include-header: Fwpsk.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows Vista.
req.target-min-winversvr: 
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
req.typenames: FWPS_INCOMING_VALUES0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPS_INCOMING_VALUES0_
 - fwpstypes/FWPS_INCOMING_VALUES0_
 - FWPS_INCOMING_VALUES0
 - fwpstypes/FWPS_INCOMING_VALUES0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fwpstypes.h
api_name:
 - FWPS_INCOMING_VALUES0
---

# FWPS_INCOMING_VALUES0 structure


## -description

The <b>FWPS_INCOMING_VALUES0</b> structure defines data values that are passed by the filter engine to a
  callout's 
  <a href="/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn0">classifyFn</a> callout function.
<div class="alert"><b>Note</b>  <b>FWPS_INCOMING_VALUES0</b> is a specific version of <b>FWPS_INCOMING_VALUES</b>. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields

### -field layerId

The run-time filtering layer identifier for the filtering layer at which the data values were
     obtained. For more information, see 
     <a href="/windows/desktop/FWP/management-filtering-layer-identifiers-">Run-time Filtering Layer
     Identifiers</a>.

### -field valueCount

The number of 
     [FWPS_INCOMING_VALUE0](/windows/desktop/api/fwpstypes/ns-fwpstypes-fwps_incoming_value0) structures in the
     array pointed to by the 
     <b>incomingValue</b> member.

### -field incomingValue

A pointer to an array of 
     [FWPS_INCOMING_VALUE0](/windows/desktop/api/fwpstypes/ns-fwpstypes-fwps_incoming_value0) structures that
     contain the data values.

## -remarks

The filter engine passes a pointer to an FWPS_INCOMING_VALUES0 structure to a callout's 

    <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn0">classifyFn</a> callout function. 
    The values in this array depend on the **layerId**; each layer has an associated set of available indexes as outlined in the **FWPS_FIELDS_&lt;LAYER_ID&gt;** enumerations. 
    For example, for the **ALE_AUTH_CONNECT_V4** layer, the available indexes are listed in the [FWPS_FIELDS_ALE_AUTH_CONNECT_V4 enumeration](windows-hardware/drivers/ddi/fwpsk/ne-fwpsk-fwps_fields_ale_auth_connect_v4_). 





## -see-also

[FWPS_INCOMING_VALUE0](/windows/desktop/api/fwpstypes/ns-fwpstypes-fwps_incoming_value0)



<a href="/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn0">classifyFn</a>