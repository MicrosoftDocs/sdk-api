---
UID: NS:opmapi._OPM_CONNECTED_HDCP_DEVICE_INFORMATION
title: "_OPM_CONNECTED_HDCP_DEVICE_INFORMATION"
author: windows-sdk-content
description: Contains the result from an OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION query.
old-location: mf\opm_connected_hdcp_device_information.htm
tech.root: medfound
ms.assetid: 1fb59959-782b-44e8-81b1-eca3c32a0783
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: OPM_CONNECTED_HDCP_DEVICE_INFORMATION, OPM_CONNECTED_HDCP_DEVICE_INFORMATION structure [Media Foundation], OPM_HDCP_FLAG_NONE, OPM_HDCP_FLAG_REPEATER, _OPM_CONNECTED_HDCP_DEVICE_INFORMATION, mf.opm_connected_hdcp_device_information, opmapi/OPM_CONNECTED_HDCP_DEVICE_INFORMATION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - opmapi.h
api_name:
 - OPM_CONNECTED_HDCP_DEVICE_INFORMATION
product: Windows
targetos: Windows
req.typenames: OPM_CONNECTED_HDCP_DEVICE_INFORMATION
req.redist: 
---

# _OPM_CONNECTED_HDCP_DEVICE_INFORMATION structure


## -description


Contains the result from an <a href="https://msdn.microsoft.com/71fa9a99-83e4-4b27-9fd1-5a9dc3070820">OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION</a> query.


## -struct-fields




### -field rnRandomNumber

An <a href="https://msdn.microsoft.com/d3a5be4b-39d1-43da-b87e-ab4dd7815262">OPM_RANDOM_NUMBER</a> structure. This structure contains the same 128-bit random number that the application sent to the driver in the <a href="https://msdn.microsoft.com/8959c7d1-9a78-497f-8841-d3e61e9db6a3">OPM_GET_INFO_PARAMETERS</a> or <a href="https://msdn.microsoft.com/46c0c426-9730-4a0e-ab95-03b240bd55f0">OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS</a> structure.


### -field ulStatusFlags

A bitwise <b>OR</b> of <a href="https://msdn.microsoft.com/d6d85fd4-e735-4610-93e0-bb2b1782f11b">OPM Status Flags</a>.


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

An <a href="https://msdn.microsoft.com/79c0e5e5-62ef-4b8a-9e3b-3a9482731b16">OPM_HDCP_KEY_SELECTION_VECTOR</a> structure that contains the device's key selection vector (KSV). This is the value named <i>Bksv</i> in the HDCP specification.


### -field Reserved

Reserved for future use. Fill this array with zeros.


### -field Reserved2

Reserved for future use. Fill this array with zeros. 


### -field Reserved3

Reserved for future use. Fill this array with zeros.


## -remarks



The layout of this structure is identical to the <a href="https://msdn.microsoft.com/fd49c50d-6caa-4d2a-83c6-41ff0130160f">DXVA_COPPStatusHDCPKeyData</a> structure used in Certified Output Protection Protocol (COPP).




## -see-also




<a href="https://msdn.microsoft.com/676a60ca-393e-4b5d-89d3-50cf4b771492">OPM Structures</a>



<a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>
 

 

