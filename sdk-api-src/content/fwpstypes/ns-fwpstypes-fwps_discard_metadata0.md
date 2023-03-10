---
UID: NS:fwpstypes.FWPS_DISCARD_METADATA0_
title: FWPS_DISCARD_METADATA0 (fwpstypes.h)
description: The FWPS_DISCARD_METADATA0 structure describes the data that was discarded by the filter engine, a network layer, or a transport layer.Note  FWPS_DISCARD_METADATA0 is a specific version of FWPS_DISCARD_METADATA.
helpviewer_keywords: ["FWPS_DISCARD_METADATA0","FWPS_DISCARD_METADATA0 structure [Network Drivers Starting with Windows Vista]","fwpstypes/FWPS_DISCARD_METADATA0","netvista.fwps_discard_metadata0","wfp_ref_3_struct_3_fwps_F-O_b2c71176-0655-45cf-ac72-3fbb690fb05b.xml"]
old-location: netvista\fwps_discard_metadata0.htm
tech.root: NetVista
ms.assetid: f17076d8-b669-4bb4-a871-10c7bdc6e370
ms.date: 12/05/2018
ms.keywords: FWPS_DISCARD_METADATA0, FWPS_DISCARD_METADATA0 structure [Network Drivers Starting with Windows Vista], fwpstypes/FWPS_DISCARD_METADATA0, netvista.fwps_discard_metadata0, wfp_ref_3_struct_3_fwps_F-O_b2c71176-0655-45cf-ac72-3fbb690fb05b.xml
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
req.typenames: FWPS_DISCARD_METADATA0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPS_DISCARD_METADATA0_
 - fwpstypes/FWPS_DISCARD_METADATA0_
 - FWPS_DISCARD_METADATA0
 - fwpstypes/FWPS_DISCARD_METADATA0
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
 - FWPS_DISCARD_METADATA0
---

# FWPS_DISCARD_METADATA0 structure


## -description

The <b>FWPS_DISCARD_METADATA0</b> structure describes the data that was discarded by the filter engine, a
  network layer, or a transport layer.
<div class="alert"><b>Note</b>  <b>FWPS_DISCARD_METADATA0</b> is a specific version of <b>FWPS_DISCARD_METADATA</b>. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields

### -field discardModule

An 
     [FWPS_DISCARD_MODULE0](/windows/desktop/api/fwpstypes/ne-fwpstypes-fwps_discard_module0) type that indicates
     the type of module that discarded the data.

### -field discardReason

A UINT32 value that specifies why the data was discarded. For a description of the discard reason identifiers for each type of module, see <a href="/windows-hardware/drivers/network/general-discard-reasons">Discard Reason Identifiers</a>.



### -field filterId

A UINT64 value that specifies the run-time identifier for the filter in the filter engine that caused the data to be discarded.

## -remarks

The FWPS_DISCARD_METADATA0 structure contains valid data only if the FWPS_METADATA_FIELD_DISCARD_REASON flag is set in the 
    <b>currentMetadataValues</b> member of the 
    <a href="/windows-hardware/drivers/ddi/content/fwpsk/ns-fwpsk-fwps_incoming_metadata_values0_">FWPS_INCOMING_METADATA_VALUES0</a> structure that the filter engine passes to a callout's 
    <a href="/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn0">classifyFn</a> callout function.

## -see-also

[FWPS_DISCARD_MODULE0](/windows/desktop/api/fwpstypes/ne-fwpstypes-fwps_discard_module0)

<a href="/windows-hardware/drivers/ddi/content/fwpsk/ns-fwpsk-fwps_incoming_metadata_values0_">FWPS_INCOMING_METADATA_VALUES0</a>

<a href="/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn0">classifyFn</a>