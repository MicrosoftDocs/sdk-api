---
UID: NS:mfidl._MFRR_COMPONENT_HASH_INFO
title: MFRR_COMPONENT_HASH_INFO (mfidl.h)
description: Contains information about a revoked component.
helpviewer_keywords: ["*PMFRR_COMPONENT_HASH_INFO","MFRR_COMPONENT_HASH_INFO","MFRR_COMPONENT_HASH_INFO structure [Media Foundation]","MF_BOOT_DRIVER_VERIFICATION_FAILED","MF_COMPONENT_CERT_REVOKED","MF_COMPONENT_HS_CERT_REVOKED","MF_COMPONENT_INVALID_EKU","MF_COMPONENT_INVALID_ROOT","MF_COMPONENT_LS_CERT_REVOKED","MF_COMPONENT_REVOKED","MF_GRL_ABSENT","MF_GRL_LOAD_FAILED","MF_INVALID_GRL_SIGNATURE","MF_KERNEL_MODE_COMPONENT_LOAD","MF_MINCRYPT_FAILURE","MF_TEST_SIGNED_COMPONENT_LOADING","MF_USER_MODE_COMPONENT_LOAD","PMFRR_COMPONENT_HASH_INFO","PMFRR_COMPONENT_HASH_INFO structure pointer [Media Foundation]","e23bc68c-b62e-4483-b2a7-a7de7376697f","mf.mfrr_component_hash_info","mfidl/MFRR_COMPONENT_HASH_INFO","mfidl/PMFRR_COMPONENT_HASH_INFO"]
old-location: mf\mfrr_component_hash_info.htm
tech.root: mf
ms.assetid: e23bc68c-b62e-4483-b2a7-a7de7376697f
ms.date: 12/05/2018
ms.keywords: '*PMFRR_COMPONENT_HASH_INFO, MFRR_COMPONENT_HASH_INFO, MFRR_COMPONENT_HASH_INFO structure [Media Foundation], MF_BOOT_DRIVER_VERIFICATION_FAILED, MF_COMPONENT_CERT_REVOKED, MF_COMPONENT_HS_CERT_REVOKED, MF_COMPONENT_INVALID_EKU, MF_COMPONENT_INVALID_ROOT, MF_COMPONENT_LS_CERT_REVOKED, MF_COMPONENT_REVOKED, MF_GRL_ABSENT, MF_GRL_LOAD_FAILED, MF_INVALID_GRL_SIGNATURE, MF_KERNEL_MODE_COMPONENT_LOAD, MF_MINCRYPT_FAILURE, MF_TEST_SIGNED_COMPONENT_LOADING, MF_USER_MODE_COMPONENT_LOAD, PMFRR_COMPONENT_HASH_INFO, PMFRR_COMPONENT_HASH_INFO structure pointer [Media Foundation], e23bc68c-b62e-4483-b2a7-a7de7376697f, mf.mfrr_component_hash_info, mfidl/MFRR_COMPONENT_HASH_INFO, mfidl/PMFRR_COMPONENT_HASH_INFO'
req.header: mfidl.h
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
req.typenames: MFRR_COMPONENT_HASH_INFO, *PMFRR_COMPONENT_HASH_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFRR_COMPONENT_HASH_INFO
 - mfidl/_MFRR_COMPONENT_HASH_INFO
 - PMFRR_COMPONENT_HASH_INFO
 - mfidl/PMFRR_COMPONENT_HASH_INFO
 - MFRR_COMPONENT_HASH_INFO
 - mfidl/MFRR_COMPONENT_HASH_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFRR_COMPONENT_HASH_INFO
---

# MFRR_COMPONENT_HASH_INFO structure


## -description

Contains information about a revoked component.

## -struct-fields

### -field ulReason

Specifies the reason for the revocation. The following values are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MF_BOOT_DRIVER_VERIFICATION_FAILED"></a><a id="mf_boot_driver_verification_failed"></a><dl>
<dt><b>MF_BOOT_DRIVER_VERIFICATION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
A boot driver could not be verified.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_COMPONENT_CERT_REVOKED"></a><a id="mf_component_cert_revoked"></a><dl>
<dt><b>MF_COMPONENT_CERT_REVOKED</b></dt>
</dl>
</td>
<td width="60%">
A certificate in a trusted component's certificate chain was revoked.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_COMPONENT_HS_CERT_REVOKED"></a><a id="mf_component_hs_cert_revoked"></a><dl>
<dt><b>MF_COMPONENT_HS_CERT_REVOKED</b></dt>
</dl>
</td>
<td width="60%">
The high-security certificate for authenticating the protected environment (PE) was revoked.

The high-security certificate is typically used by ITAs that handle high-definition content and next-generation formats such as HD-DVD.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_COMPONENT_INVALID_EKU"></a><a id="mf_component_invalid_eku"></a><dl>
<dt><b>MF_COMPONENT_INVALID_EKU</b></dt>
</dl>
</td>
<td width="60%">
A certificate's extended key usage (EKU) object is invalid.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_COMPONENT_INVALID_ROOT"></a><a id="mf_component_invalid_root"></a><dl>
<dt><b>MF_COMPONENT_INVALID_ROOT</b></dt>
</dl>
</td>
<td width="60%">
The root certificate is not valid.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_COMPONENT_LS_CERT_REVOKED"></a><a id="mf_component_ls_cert_revoked"></a><dl>
<dt><b>MF_COMPONENT_LS_CERT_REVOKED</b></dt>
</dl>
</td>
<td width="60%">
The low-security certificate for authenticating the PE was revoked.

The low-security certificate is typically used by ITAs that handle standard-definition content and current-generation formats.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_COMPONENT_REVOKED"></a><a id="mf_component_revoked"></a><dl>
<dt><b>MF_COMPONENT_REVOKED</b></dt>
</dl>
</td>
<td width="60%">
A trusted component was revoked.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_GRL_ABSENT"></a><a id="mf_grl_absent"></a><dl>
<dt><b>MF_GRL_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
The GRL was not found.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_GRL_LOAD_FAILED"></a><a id="mf_grl_load_failed"></a><dl>
<dt><b>MF_GRL_LOAD_FAILED</b></dt>
</dl>
</td>
<td width="60%">
Could not load the global revocation list (GRL).

</td>
</tr>
<tr>
<td width="40%"><a id="MF_INVALID_GRL_SIGNATURE"></a><a id="mf_invalid_grl_signature"></a><dl>
<dt><b>MF_INVALID_GRL_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
The GRL signature is invalid.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_MINCRYPT_FAILURE"></a><a id="mf_mincrypt_failure"></a><dl>
<dt><b>MF_MINCRYPT_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
A certificate chain was not well-formed, or a boot driver is unsigned or is signed with an untrusted certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_TEST_SIGNED_COMPONENT_LOADING"></a><a id="mf_test_signed_component_loading"></a><dl>
<dt><b>MF_TEST_SIGNED_COMPONENT_LOADING</b></dt>
</dl>
</td>
<td width="60%">
A component was signed by a test certificate.

</td>
</tr>
</table>
 

In addition, one of the following flags might be present, indicating the type of component that failed to load.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MF_USER_MODE_COMPONENT_LOAD"></a><a id="mf_user_mode_component_load"></a><dl>
<dt><b>MF_USER_MODE_COMPONENT_LOAD</b></dt>
</dl>
</td>
<td width="60%">
User-mode component.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_KERNEL_MODE_COMPONENT_LOAD"></a><a id="mf_kernel_mode_component_load"></a><dl>
<dt><b>MF_KERNEL_MODE_COMPONENT_LOAD</b></dt>
</dl>
</td>
<td width="60%">
Kernel-mode component.

</td>
</tr>
</table>

### -field rgHeaderHash

Contains a hash of the file header.

### -field rgPublicKeyHash

Contains a hash of the public key in the component's certificate.

### -field wszName

File name of the revoked component.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>