---
UID: NS:ntenclv.VBS_ENCLAVE_REPORT_VARDATA_HEADER
title: VBS_ENCLAVE_REPORT_VARDATA_HEADER (ntenclv.h)
description: Describes the format of a variable data block contained in a report that the EnclaveGetAttestationReport function generates.
helpviewer_keywords: ["VBS_ENCLAVE_REPORT_VARDATA_HEADER","VBS_ENCLAVE_REPORT_VARDATA_HEADER structure","VBS_ENCLAVE_VARDATA_INVALID","VBS_ENCLAVE_VARDATA_MODULE","base.vbs_enclave_report_vardata_header","ntenclv/VBS_ENCLAVE_REPORT_VARDATA_HEADER"]
old-location: base\vbs_enclave_report_vardata_header.htm
tech.root: base
ms.assetid: A0B02839-E8F4-45A1-B2BA-73E6EF9DA7C8
ms.date: 12/05/2018
ms.keywords: VBS_ENCLAVE_REPORT_VARDATA_HEADER, VBS_ENCLAVE_REPORT_VARDATA_HEADER structure, VBS_ENCLAVE_VARDATA_INVALID, VBS_ENCLAVE_VARDATA_MODULE, base.vbs_enclave_report_vardata_header, ntenclv/VBS_ENCLAVE_REPORT_VARDATA_HEADER
req.header: ntenclv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: VBS_ENCLAVE_REPORT_VARDATA_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VBS_ENCLAVE_REPORT_VARDATA_HEADER
 - ntenclv/VBS_ENCLAVE_REPORT_VARDATA_HEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntenclv.h
api_name:
 - VBS_ENCLAVE_REPORT_VARDATA_HEADER
---

# VBS_ENCLAVE_REPORT_VARDATA_HEADER structure


## -description

Describes the format of a variable data block contained in a report that the <a href="/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport">EnclaveGetAttestationReport</a> function generates.

## -struct-fields

### -field DataType

The type of the variable data block.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VBS_ENCLAVE_VARDATA_INVALID"></a><a id="vbs_enclave_vardata_invalid"></a><dl>
<dt><b>VBS_ENCLAVE_VARDATA_INVALID</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The variable data block is not valid.

</td>
</tr>
<tr>
<td width="40%"><a id="VBS_ENCLAVE_VARDATA_MODULE"></a><a id="vbs_enclave_vardata_module"></a><dl>
<dt><b>VBS_ENCLAVE_VARDATA_MODULE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The variable data block is a module.

</td>
</tr>
</table>

### -field Size

The size of this variable data block, including the header, in bytes.

## -remarks

An enclave attestation report includes zero or  variable data blocks. These variable data blocks consist of the following items:

<ul>
<li>A <b>VBS_ENCLAVE_REPORT_VARDATA_HEADER</b> structure that describes the format of the variable data block. </li>
<li>The data described by the <b>VBS_ENCLAVE_REPORT_VARDATA_HEADER</b> structure. If the value of the <b>DataType</b> member of the <b>VBS_ENCLAVE_REPORT_VARDATA_HEADER</b> structure is  <b>VBS_ENCLAVE_VARDATA_MODULE</b>, this data is a <a href="/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_module">VBS_ENCLAVE_REPORT_MODULE</a> structure.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport">EnclaveGetAttestationReport</a>



<a href="/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report">VBS_ENCLAVE_REPORT</a>



<a href="/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_module">VBS_ENCLAVE_REPORT_MODULE</a>