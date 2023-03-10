---
UID: NS:opmapi._OPM_CONNECTED_HDCP_DEVICE_INFORMATION
title: OPM_CONNECTED_HDCP_DEVICE_INFORMATION (opmapi.h)
description: Contains the result from an OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION query.
helpviewer_keywords: ["OPM_CONNECTED_HDCP_DEVICE_INFORMATION","OPM_CONNECTED_HDCP_DEVICE_INFORMATION structure [Media Foundation]","OPM_HDCP_FLAG_NONE","OPM_HDCP_FLAG_REPEATER","mf.opm_connected_hdcp_device_information","opmapi/OPM_CONNECTED_HDCP_DEVICE_INFORMATION"]
old-location: mf\opm_connected_hdcp_device_information.htm
tech.root: mf
ms.assetid: 1fb59959-782b-44e8-81b1-eca3c32a0783
ms.date: 12/05/2018
ms.keywords: OPM_CONNECTED_HDCP_DEVICE_INFORMATION, OPM_CONNECTED_HDCP_DEVICE_INFORMATION structure [Media Foundation], OPM_HDCP_FLAG_NONE, OPM_HDCP_FLAG_REPEATER, mf.opm_connected_hdcp_device_information, opmapi/OPM_CONNECTED_HDCP_DEVICE_INFORMATION
req.header: opmapi.h
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
req.typenames: OPM_CONNECTED_HDCP_DEVICE_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OPM_CONNECTED_HDCP_DEVICE_INFORMATION
 - opmapi/_OPM_CONNECTED_HDCP_DEVICE_INFORMATION
 - OPM_CONNECTED_HDCP_DEVICE_INFORMATION
 - opmapi/OPM_CONNECTED_HDCP_DEVICE_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - opmapi.h
api_name:
 - OPM_CONNECTED_HDCP_DEVICE_INFORMATION
---

# OPM_CONNECTED_HDCP_DEVICE_INFORMATION structure


## -description

Contains the result from an <a href="/windows/desktop/medfound/opm-get-connected-hdcp-device-information">OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION</a> query.

## -struct-fields

### -field rnRandomNumber

An <a href="/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_random_number">OPM_RANDOM_NUMBER</a> structure. This structure contains the same 128-bit random number that the application sent to the driver in the <a href="/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters">OPM_GET_INFO_PARAMETERS</a> or <a href="/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation">OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS</a> structure.

### -field ulStatusFlags

A bitwise <b>OR</b> of <a href="/windows/desktop/medfound/opm-status-flags">OPM Status Flags</a>.

### -field ulHDCPFlags

A value that indicates whether the connected device is an HDCP repeater.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OPM_HDCP_FLAG_NONE"></a><a id="opm_hdcp_flag_none"></a><dl>
<dt><b>OPM_HDCP_FLAG_NONE</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
The device is not an HDCP repeater.

</td>
</tr>
<tr>
<td width="40%"><a id="OPM_HDCP_FLAG_REPEATER"></a><a id="opm_hdcp_flag_repeater"></a><dl>
<dt><b>OPM_HDCP_FLAG_REPEATER</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The device is an HDCP repeater.

</td>
</tr>
</table>

### -field ksvB

An <a href="/windows/desktop/api/opmapi/ns-opmapi-opm_hdcp_key_selection_vector">OPM_HDCP_KEY_SELECTION_VECTOR</a> structure that contains the device's key selection vector (KSV). This is the value named <i>Bksv</i> in the HDCP specification.

### -field Reserved

Reserved for future use. Fill this array with zeros.

### -field Reserved2

Reserved for future use. Fill this array with zeros.

### -field Reserved3

Reserved for future use. Fill this array with zeros.

## -remarks

The layout of this structure is identical to the <a href="/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata">DXVA_COPPStatusHDCPKeyData</a> structure used in Certified Output Protection Protocol (COPP).

## -see-also

<a href="/windows/desktop/medfound/opm-structures">OPM Structures</a>



<a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>