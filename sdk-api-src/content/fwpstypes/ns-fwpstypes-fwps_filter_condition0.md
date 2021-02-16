---
UID: NS:fwpstypes.FWPS_FILTER_CONDITION0_
title: FWPS_FILTER_CONDITION0 (fwpstypes.h)
description: The FWPS_FILTER_CONDITION0 structure defines a run-time filtering condition for a filter.Note  FWPS_FILTER_CONDITION0 is a specific version of FWPS_FILTER_CONDITION.
helpviewer_keywords: ["FWPS_FILTER_CONDITION0","FWPS_FILTER_CONDITION0 structure [Network Drivers Starting with Windows Vista]","fwpstypes/FWPS_FILTER_CONDITION0","netvista.fwps_filter_condition0","wfp_ref_3_struct_3_fwps_F-O_93287819-7faf-41d5-a128-946293c1eb73.xml"]
old-location: netvista\fwps_filter_condition0.htm
tech.root: NetVista
ms.assetid: d4a20939-4866-4402-9b29-d94c2170807c
ms.date: 12/05/2018
ms.keywords: FWPS_FILTER_CONDITION0, FWPS_FILTER_CONDITION0 structure [Network Drivers Starting with Windows Vista], fwpstypes/FWPS_FILTER_CONDITION0, netvista.fwps_filter_condition0, wfp_ref_3_struct_3_fwps_F-O_93287819-7faf-41d5-a128-946293c1eb73.xml
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
req.typenames: FWPS_FILTER_CONDITION0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPS_FILTER_CONDITION0_
 - fwpstypes/FWPS_FILTER_CONDITION0_
 - FWPS_FILTER_CONDITION0
 - fwpstypes/FWPS_FILTER_CONDITION0
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
 - FWPS_FILTER_CONDITION0
---

# FWPS_FILTER_CONDITION0 structure


## -description

The <b>FWPS_FILTER_CONDITION0</b> structure defines a run-time filtering condition for a filter.
<div class="alert"><b>Note</b>  <b>FWPS_FILTER_CONDITION0</b> is a specific version of <b>FWPS_FILTER_CONDITION</b>. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields

### -field fieldId

The data field identifier for the data field tested by this filtering condition. The meaning of
     the numeric value of this member is specific to the filtering layer specified by the 
     <b>layerId</b> member. For a description of the data field identifiers for each filtering layer, see 
     <a href="/windows-hardware/drivers/network/data-field-identifiers">Data Field Identifiers</a>.

### -field reserved

Reserved for system use. Callout drivers should ignore this member.

### -field matchType

An 
     <a href="/previous-versions/windows/hardware/drivers/ff552437(v=vs.85)">FWP_MATCH_TYPE</a> value that specifies the type
     of match that the filter engine is to test on the data field to check whether the filtering condition is
     true.

### -field conditionValue

An 
     <a href="/previous-versions/windows/hardware/drivers/ff552430(v=vs.85)">FWP_CONDITION_VALUE0</a> structure that
     specifies the value against which the data field is tested.

## -remarks

The 
    <b>filterCondition</b> member of the 
    [FWPS_FILTER0](/windows/desktop/api/fwpstypes/ns-fwpstypes-fwps_filter0) structure points to an array of
    FWPS_FILTER_CONDITION0 structures that specify the run-time filtering conditions for a filter.

## -see-also

[FWPS_FILTER0](/windows/desktop/api/fwpstypes/ns-fwpstypes-fwps_filter0)



<a href="/previous-versions/windows/hardware/drivers/ff552430(v=vs.85)">FWP_CONDITION_VALUE0</a>



<a href="/previous-versions/windows/hardware/drivers/ff552437(v=vs.85)">FWP_MATCH_TYPE</a>