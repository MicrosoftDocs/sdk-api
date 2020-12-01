---
UID: NS:fwpstypes.FWPS_INBOUND_FRAGMENT_METADATA0_
title: FWPS_INBOUND_FRAGMENT_METADATA0 (fwpstypes.h)
description: The FWPS_INBOUND_FRAGMENT_METADATA0 structure describes the fragment data for a received packet fragment.Note  FWPS_INBOUND_FRAGMENT_METADATA0 is a specific version of FWPS_INBOUND_FRAGMENT_METADATA.
helpviewer_keywords: ["FWPS_INBOUND_FRAGMENT_METADATA0","FWPS_INBOUND_FRAGMENT_METADATA0 structure [Network Drivers Starting with Windows Vista]","fwpstypes/FWPS_INBOUND_FRAGMENT_METADATA0","netvista.fwps_inbound_fragment_metadata0","wfp_ref_3_struct_3_fwps_F-O_f826ecbb-5bd5-4ca3-a13a-49b385ca29c4.xml"]
old-location: netvista\fwps_inbound_fragment_metadata0.htm
tech.root: NetVista
ms.assetid: 9bead001-7ea7-4a51-8a7c-82fe01017dd7
ms.date: 12/05/2018
ms.keywords: FWPS_INBOUND_FRAGMENT_METADATA0, FWPS_INBOUND_FRAGMENT_METADATA0 structure [Network Drivers Starting with Windows Vista], fwpstypes/FWPS_INBOUND_FRAGMENT_METADATA0, netvista.fwps_inbound_fragment_metadata0, wfp_ref_3_struct_3_fwps_F-O_f826ecbb-5bd5-4ca3-a13a-49b385ca29c4.xml
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
req.typenames: FWPS_INBOUND_FRAGMENT_METADATA0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPS_INBOUND_FRAGMENT_METADATA0_
 - fwpstypes/FWPS_INBOUND_FRAGMENT_METADATA0_
 - FWPS_INBOUND_FRAGMENT_METADATA0
 - fwpstypes/FWPS_INBOUND_FRAGMENT_METADATA0
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
 - FWPS_INBOUND_FRAGMENT_METADATA0
---

# FWPS_INBOUND_FRAGMENT_METADATA0 structure


## -description

The <b>FWPS_INBOUND_FRAGMENT_METADATA0</b> structure describes the fragment data for a received packet
  fragment.
<div class="alert"><b>Note</b>  <b>FWPS_INBOUND_FRAGMENT_METADATA0</b> is a specific version of <b>FWPS_INBOUND_FRAGMENT_METADATA</b>. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields

### -field fragmentIdentification

A value that identifies the packet to which the packet fragment belongs.

### -field fragmentOffset

A value that specifies the offset, in bytes, of the packet fragment from the beginning of the
     packet.

### -field fragmentLength

A value that specifies the length, in bytes, of the packet fragment.

## -remarks

The FWPS_INBOUND_FRAGMENT_METADATA0 structure contains valid data only if the
    FWPS_METADATA_FIELD_FRAGMENT_DATA flag is set in the 
    <b>currentMetadataValues</b> member of the 
    <a href="/windows-hardware/drivers/ddi/content/fwpsk/ns-fwpsk-fwps_incoming_metadata_values0_">FWPS_INCOMING_METADATA_VALUES0</a> structure that the filter engine passes to a callout's 
    <a href="/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn0">classifyFn</a> callout function.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/fwpsk/ns-fwpsk-fwps_incoming_metadata_values0_">FWPS_INCOMING_METADATA_VALUES0</a>



<a href="/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn0">classifyFn</a>