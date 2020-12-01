---
UID: NS:iketypes.IKEEXT_CERT_ROOT_CONFIG0_
title: IKEEXT_CERT_ROOT_CONFIG0 (iketypes.h)
description: Stores the IKE, AuthIP, or IKEv2 certificate root configuration.
helpviewer_keywords: ["IKEEXT_CERT_FLAG_DISABLE_REQUEST_PAYLOAD","IKEEXT_CERT_FLAG_ENABLE_ACCOUNT_MAPPING","IKEEXT_CERT_FLAG_FOLLOW_RENEWAL_CERTIFICATE","IKEEXT_CERT_FLAG_IGNORE_INIT_CERT_MAP_FAILURE","IKEEXT_CERT_FLAG_INTERMEDIATE_CA","IKEEXT_CERT_FLAG_PREFER_NAP_CERTIFICATE_OUTBOUND","IKEEXT_CERT_FLAG_SELECT_NAP_CERTIFICATE","IKEEXT_CERT_FLAG_USE_NAP_CERTIFICATE","IKEEXT_CERT_FLAG_VERIFY_NAP_CERTIFICATE","IKEEXT_CERT_ROOT_CONFIG0","IKEEXT_CERT_ROOT_CONFIG0 structure [Filtering]","fwp.ikeext_cert_root_config0","iketypes/IKEEXT_CERT_ROOT_CONFIG0"]
old-location: fwp\ikeext_cert_root_config0.htm
tech.root: fwp
ms.assetid: 820da66b-670e-490e-bba4-c2b0afb6dfd1
ms.date: 12/05/2018
ms.keywords: IKEEXT_CERT_FLAG_DISABLE_REQUEST_PAYLOAD, IKEEXT_CERT_FLAG_ENABLE_ACCOUNT_MAPPING, IKEEXT_CERT_FLAG_FOLLOW_RENEWAL_CERTIFICATE, IKEEXT_CERT_FLAG_IGNORE_INIT_CERT_MAP_FAILURE, IKEEXT_CERT_FLAG_INTERMEDIATE_CA, IKEEXT_CERT_FLAG_PREFER_NAP_CERTIFICATE_OUTBOUND, IKEEXT_CERT_FLAG_SELECT_NAP_CERTIFICATE, IKEEXT_CERT_FLAG_USE_NAP_CERTIFICATE, IKEEXT_CERT_FLAG_VERIFY_NAP_CERTIFICATE, IKEEXT_CERT_ROOT_CONFIG0, IKEEXT_CERT_ROOT_CONFIG0 structure [Filtering], fwp.ikeext_cert_root_config0, iketypes/IKEEXT_CERT_ROOT_CONFIG0
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IKEEXT_CERT_ROOT_CONFIG0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_CERT_ROOT_CONFIG0_
 - iketypes/IKEEXT_CERT_ROOT_CONFIG0_
 - IKEEXT_CERT_ROOT_CONFIG0
 - iketypes/IKEEXT_CERT_ROOT_CONFIG0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_CERT_ROOT_CONFIG0
---

# IKEEXT_CERT_ROOT_CONFIG0 structure


## -description

The <b>IKEEXT_CERT_ROOT_CONFIG0</b> structure stores the IKE, AuthIP, or IKEv2 certificate root configuration.

## -struct-fields

### -field certData

X509/ASN.1 encoded name of the certificate root.

See [FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob) for more information.

### -field flags

A combination of the following values.

<table>
<tr>
<th>IKE/AuthIP/IKEv2 certificate flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_CERT_FLAG_ENABLE_ACCOUNT_MAPPING"></a><a id="ikeext_cert_flag_enable_account_mapping"></a><dl>
<dt><b>IKEEXT_CERT_FLAG_ENABLE_ACCOUNT_MAPPING</b></dt>
</dl>
</td>
<td width="60%">
Enable certificate-to-account mapping for the end-host certificate that chains to this root.

</td>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_CERT_FLAG_DISABLE_REQUEST_PAYLOAD"></a><a id="ikeext_cert_flag_disable_request_payload"></a><dl>
<dt><b>IKEEXT_CERT_FLAG_DISABLE_REQUEST_PAYLOAD</b></dt>
</dl>
</td>
<td width="60%">
Do not send a Cert request payload for this root.

</td>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_CERT_FLAG_USE_NAP_CERTIFICATE"></a><a id="ikeext_cert_flag_use_nap_certificate"></a><dl>
<dt><b>IKEEXT_CERT_FLAG_USE_NAP_CERTIFICATE</b></dt>
</dl>
</td>
<td width="60%">
Enable Network Access Protection (NAP) certificate handling.

</td>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_CERT_FLAG_INTERMEDIATE_CA"></a><a id="ikeext_cert_flag_intermediate_ca"></a><dl>
<dt><b>IKEEXT_CERT_FLAG_INTERMEDIATE_CA</b></dt>
</dl>
</td>
<td width="60%">
The corresponding Certification Authority (CA) can be an intermediate CA and does not have to be a ROOT CA.

If this flag is not specified, the name will have to refer to a ROOT CA.

</td>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_CERT_FLAG_IGNORE_INIT_CERT_MAP_FAILURE"></a><a id="ikeext_cert_flag_ignore_init_cert_map_failure"></a><dl>
<dt><b>IKEEXT_CERT_FLAG_IGNORE_INIT_CERT_MAP_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
Ignore mapping failures on the initiator. Available only for IKE and IKEv2.

Can be set only if <b>IKEEXT_CERT_FLAG_ENABLE_ACCOUNT_MAPPING</b> is also specified. By default, IKE and IKEv2 will not ignore certificate to account mapping failures, even on the initiator.

Available only on Windows 7, Windows Server 2008 R2, and later.

</td>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_CERT_FLAG_PREFER_NAP_CERTIFICATE_OUTBOUND"></a><a id="ikeext_cert_flag_prefer_nap_certificate_outbound"></a><dl>
<dt><b>IKEEXT_CERT_FLAG_PREFER_NAP_CERTIFICATE_OUTBOUND</b></dt>
</dl>
</td>
<td width="60%">
NAP certificates will be preferred for local certificate selection.

</td>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_CERT_FLAG_SELECT_NAP_CERTIFICATE"></a><a id="ikeext_cert_flag_select_nap_certificate"></a><dl>
<dt><b>IKEEXT_CERT_FLAG_SELECT_NAP_CERTIFICATE</b></dt>
</dl>
</td>
<td width="60%">
Select a NAP certificate for outbound.

Available only on Windows 8 and Windows Server 2012.

</td>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_CERT_FLAG_VERIFY_NAP_CERTIFICATE"></a><a id="ikeext_cert_flag_verify_nap_certificate"></a><dl>
<dt><b>IKEEXT_CERT_FLAG_VERIFY_NAP_CERTIFICATE</b></dt>
</dl>
</td>
<td width="60%">
Verify that the inbound certificate is NAP.

Available only on Windows 8 and Windows Server 2012.

</td>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_CERT_FLAG_FOLLOW_RENEWAL_CERTIFICATE"></a><a id="ikeext_cert_flag_follow_renewal_certificate"></a><dl>
<dt><b>IKEEXT_CERT_FLAG_FOLLOW_RENEWAL_CERTIFICATE</b></dt>
</dl>
</td>
<td width="60%">
Follow the renewal property on the certificate when selecting local certificate for outbound.

Only applicable when the hash of the certificate is specified.

Available only on Windows 8 and Windows Server 2012.

</td>
</tr>
</table>

## -remarks

<b>IKEEXT_CERT_ROOT_CONFIG0</b> is a specific implementation of IKEEXT_CERT_ROOT_CONFIG. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>