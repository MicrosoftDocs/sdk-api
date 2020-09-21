---
UID: NS:fwpstypes.FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0_
title: FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0 (fwpstypes.h)
description: The FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0 structure specifies a template for application layer enforcement (ALE) endpoints to be enumerated.Note  FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0 is a specific version of FWPS_ALE_ENDPOINT_ENUM_TEMPLATE.
helpviewer_keywords: ["FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0","FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0 structure [Network Drivers Starting with Windows Vista]","fwpstypes/FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0","netvista.fwps_ale_endpoint_enum_template0","wfp_ref_3_struct_3_fwps_A-E_1d06d4d7-6e8f-4f8d-b57e-96292a680e68.xml"]
old-location: netvista\fwps_ale_endpoint_enum_template0.htm
tech.root: NetVista
ms.assetid: 7875bf42-4510-4af1-8f24-4b9f1d945100
ms.date: 12/05/2018
ms.keywords: FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0, FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0 structure [Network Drivers Starting with Windows Vista], fwpstypes/FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0, netvista.fwps_ale_endpoint_enum_template0, wfp_ref_3_struct_3_fwps_A-E_1d06d4d7-6e8f-4f8d-b57e-96292a680e68.xml
req.header: fwpstypes.h
req.include-header: Fwpsk.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows 7.
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
req.typenames: FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0_
 - fwpstypes/FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0_
 - FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0
 - fwpstypes/FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0
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
 - FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0
---

# FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0 structure


## -description

The <b>FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0</b> structure specifies a template for application layer enforcement
  (ALE) endpoints to be enumerated.
<div class="alert"><b>Note</b>  <b>FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0</b> is a specific version of <b>FWPS_ALE_ENDPOINT_ENUM_TEMPLATE</b>. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields

### -field localSubNet

The local subnet portion of the enumeration template.

### -field remoteSubNet

The remote subnet portion of the enumeration template.

### -field ipProtocol

The IP protocol portion of the enumeration template.

### -field localPort

The local port portion of the enumeration template.

### -field remotePort

The remote port portion of the enumeration template.

## -remarks

This structure can be used to narrow the results when enumerating endpoints. If used, it is specified
    when the enumeration handle is created by calling 
    <a href="/windows-hardware/drivers/ddi/content/fwpsk/nf-fwpsk-fwpsaleendpointcreateenumhandle0">FwpsAleEndpointCreateEnumHandle0</a>. Any populated members are used to limit the enumeration results
    returned by 
    <a href="/windows-hardware/drivers/ddi/content/fwpsk/nf-fwpsk-fwpsaleendpointenum0">FwpsAleEndpointEnum0</a>.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/fwpsk/nf-fwpsk-fwpsaleendpointcreateenumhandle0">FwpsAleEndpointCreateEnumHandle0</a>



<a href="/windows-hardware/drivers/ddi/content/fwpsk/nf-fwpsk-fwpsaleendpointenum0">FwpsAleEndpointEnum0</a>