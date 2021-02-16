---
UID: NS:fwpstypes.FWPS_INCOMING_VALUE0_
title: FWPS_INCOMING_VALUE0 (fwpstypes.h)
description: The FWPS_INCOMING_VALUE0 structure defines an individual data value.Note  FWPS_INCOMING_VALUE0 is a specific version of FWPS_INCOMING_VALUE.
helpviewer_keywords: ["FWPS_INCOMING_VALUE0","FWPS_INCOMING_VALUE0 structure [Network Drivers Starting with Windows Vista]","fwpstypes/FWPS_INCOMING_VALUE0","netvista.fwps_incoming_value0","wfp_ref_3_struct_3_fwps_F-O_de0ecafa-7ade-4473-a04e-3fb924c22db0.xml"]
old-location: netvista\fwps_incoming_value0.htm
tech.root: NetVista
ms.assetid: 94a81a93-7c92-4c0a-9ac7-c2085175c1a7
ms.date: 12/05/2018
ms.keywords: FWPS_INCOMING_VALUE0, FWPS_INCOMING_VALUE0 structure [Network Drivers Starting with Windows Vista], fwpstypes/FWPS_INCOMING_VALUE0, netvista.fwps_incoming_value0, wfp_ref_3_struct_3_fwps_F-O_de0ecafa-7ade-4473-a04e-3fb924c22db0.xml
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
req.typenames: FWPS_INCOMING_VALUE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPS_INCOMING_VALUE0_
 - fwpstypes/FWPS_INCOMING_VALUE0_
 - FWPS_INCOMING_VALUE0
 - fwpstypes/FWPS_INCOMING_VALUE0
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
 - FWPS_INCOMING_VALUE0
---

# FWPS_INCOMING_VALUE0 structure


## -description

The <b>FWPS_INCOMING_VALUE0</b> structure defines an individual data value.
<div class="alert"><b>Note</b>  <b>FWPS_INCOMING_VALUE0</b> is a specific version of <b>FWPS_INCOMING_VALUE</b>. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields

### -field value

An 
     <a href="/previous-versions/windows/hardware/drivers/ff552450(v=vs.85)">FWP_VALUE0</a> structure that contains the data value.

## -remarks

The 
    [FWPS_INCOMING_VALUES0](/windows/desktop/api/fwpstypes/ns-fwpstypes-fwps_incoming_values0) structure
    contains a pointer to an array of FWPS_INCOMING_VALUE0 structures that contain the incoming data values
    that are passed to a callout's 
    <a href="/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn0">classifyFn</a> callout function.

## -see-also

[FWPS_INCOMING_VALUES0](/windows/desktop/api/fwpstypes/ns-fwpstypes-fwps_incoming_values0)



<a href="/previous-versions/windows/hardware/drivers/ff552450(v=vs.85)">FWP_VALUE0</a>



<a href="/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn0">classifyFn</a>