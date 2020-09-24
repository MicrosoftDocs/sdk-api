---
UID: NS:cryptuiapi._CRYPTUI_WIZ_DIGITAL_SIGN_INFO
title: CRYPTUI_WIZ_DIGITAL_SIGN_INFO (cryptuiapi.h)
description: Contains information about digital signing.
helpviewer_keywords: ["*PCRYPTUI_WIZ_DIGITAL_SIGN_INFO","0","CRYPTUI_WIZ_DIGITAL_SIGN_ADD_CHAIN","CRYPTUI_WIZ_DIGITAL_SIGN_ADD_CHAIN_NO_ROOT","CRYPTUI_WIZ_DIGITAL_SIGN_CERT","CRYPTUI_WIZ_DIGITAL_SIGN_INFO","CRYPTUI_WIZ_DIGITAL_SIGN_INFO structure [Security]","CRYPTUI_WIZ_DIGITAL_SIGN_PVK","CRYPTUI_WIZ_DIGITAL_SIGN_STORE","CRYPTUI_WIZ_DIGITAL_SIGN_SUBJECT_BLOB","CRYPTUI_WIZ_DIGITAL_SIGN_SUBJECT_FILE","PCRYPTUI_WIZ_DIGITAL_SIGN_INFO","PCRYPTUI_WIZ_DIGITAL_SIGN_INFO structure pointer [Security]","cryptuiapi/CRYPTUI_WIZ_DIGITAL_SIGN_INFO","cryptuiapi/PCRYPTUI_WIZ_DIGITAL_SIGN_INFO","security.cryptui_wiz_digital_sign_info"]
old-location: security\cryptui_wiz_digital_sign_info.htm
tech.root: security
ms.assetid: 22d0bc45-0f66-4f5f-87d3-0849c4327eed
ms.date: 12/05/2018
ms.keywords: '*PCRYPTUI_WIZ_DIGITAL_SIGN_INFO, 0, CRYPTUI_WIZ_DIGITAL_SIGN_ADD_CHAIN, CRYPTUI_WIZ_DIGITAL_SIGN_ADD_CHAIN_NO_ROOT, CRYPTUI_WIZ_DIGITAL_SIGN_CERT, CRYPTUI_WIZ_DIGITAL_SIGN_INFO, CRYPTUI_WIZ_DIGITAL_SIGN_INFO structure [Security], CRYPTUI_WIZ_DIGITAL_SIGN_PVK, CRYPTUI_WIZ_DIGITAL_SIGN_STORE, CRYPTUI_WIZ_DIGITAL_SIGN_SUBJECT_BLOB, CRYPTUI_WIZ_DIGITAL_SIGN_SUBJECT_FILE, PCRYPTUI_WIZ_DIGITAL_SIGN_INFO, PCRYPTUI_WIZ_DIGITAL_SIGN_INFO structure pointer [Security], cryptuiapi/CRYPTUI_WIZ_DIGITAL_SIGN_INFO, cryptuiapi/PCRYPTUI_WIZ_DIGITAL_SIGN_INFO, security.cryptui_wiz_digital_sign_info'
req.header: cryptuiapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: CRYPTUI_WIZ_DIGITAL_SIGN_INFO, *PCRYPTUI_WIZ_DIGITAL_SIGN_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPTUI_WIZ_DIGITAL_SIGN_INFO
 - cryptuiapi/_CRYPTUI_WIZ_DIGITAL_SIGN_INFO
 - PCRYPTUI_WIZ_DIGITAL_SIGN_INFO
 - cryptuiapi/PCRYPTUI_WIZ_DIGITAL_SIGN_INFO
 - CRYPTUI_WIZ_DIGITAL_SIGN_INFO
 - cryptuiapi/CRYPTUI_WIZ_DIGITAL_SIGN_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cryptuiapi.h
api_name:
 - CRYPTUI_WIZ_DIGITAL_SIGN_INFO
---

# CRYPTUI_WIZ_DIGITAL_SIGN_INFO structure


## -description

<p class="CCE_Message">[The  <b>CRYPTUI_WIZ_DIGITAL_SIGN_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPTUI_WIZ_DIGITAL_SIGN_INFO</b> structure contains information about digital signing. This structure is used by the <a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuiwizdigitalsign">CryptUIWizDigitalSign</a> function.

## -struct-fields

### -field dwSize

The size, in bytes, of the structure.

### -field dwSubjectChoice

A value that indicates the entity that is to be signed. This member is required if <b>CRYPTUI_WIZ_NO_UI</b> is specified in the <i>dwFlags</i> parameter of the <a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuiwizdigitalsign">CryptUIWizDigitalSign</a> function. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_DIGITAL_SIGN_SUBJECT_BLOB"></a><a id="cryptui_wiz_digital_sign_subject_blob"></a><dl>
<dt><b>CRYPTUI_WIZ_DIGITAL_SIGN_SUBJECT_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The memory <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> specified by the <b>pSignBlobInfo</b> member is to be signed.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_DIGITAL_SIGN_SUBJECT_FILE"></a><a id="cryptui_wiz_digital_sign_subject_file"></a><dl>
<dt><b>CRYPTUI_WIZ_DIGITAL_SIGN_SUBJECT_FILE</b></dt>
</dl>
</td>
<td width="60%">
The file specified by the <b>pwszFileName</b> member is to be signed.

</td>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
The user will be prompted for a file to sign.

</td>
</tr>
</table>

### -field pwszFileName

A pointer to a null-terminated Unicode string that contains the path and file name of the file to sign. This member is used if <b>CRYPTUI_WIZ_DIGITAL_SIGN_SUBJECT_FILE</b> is specified for the <b>dwSubjectChoice</b> member.

### -field pSignBlobInfo

A pointer to a <a href="/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_blob_info">CRYPTUI_WIZ_DIGITAL_SIGN_BLOB_INFO</a> structure that contains the BLOB to sign. This member is used if <b>CRYPTUI_WIZ_DIGITAL_SIGN_SUBJECT_BLOB</b> is specified for the <b>dwSubjectChoice</b> member.

### -field dwSigningCertChoice

A value that specifies the location of the certificate that is used to sign the entity. The default value is zero. This can be one of the following values.

<div class="alert"><b>Note</b>  If <b>CRYPTUI_WIZ_NO_UI</b> is specified in the <i>dwFlags</i> parameter of the <a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuiwizdigitalsign">CryptUIWizDigitalSign</a> function, this value must be either <b>CRYPTUI_WIZ_DIGITAL_SIGN_CERT</b> or <b>CRYPTUI_WIZ_DIGITAL_SIGN_PVK</b>.</div>
<div> </div>
<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_DIGITAL_SIGN_CERT"></a><a id="cryptui_wiz_digital_sign_cert"></a><dl>
<dt><b>CRYPTUI_WIZ_DIGITAL_SIGN_CERT</b></dt>
</dl>
</td>
<td width="60%">
The certificate is contained in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure pointed to by the <b>pSigningCertContext</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_DIGITAL_SIGN_STORE"></a><a id="cryptui_wiz_digital_sign_store"></a><dl>
<dt><b>CRYPTUI_WIZ_DIGITAL_SIGN_STORE</b></dt>
</dl>
</td>
<td width="60%">
The certificate is contained in the certificate store contained in the <a href="/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_store_info">CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO</a> structure pointed to by the <b>pSigningCertStore</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_DIGITAL_SIGN_PVK"></a><a id="cryptui_wiz_digital_sign_pvk"></a><dl>
<dt><b>CRYPTUI_WIZ_DIGITAL_SIGN_PVK</b></dt>
</dl>
</td>
<td width="60%">
The certificate is contained in the PVK file contained in the <a href="/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_cert_pvk_info">CRYPTUI_WIZ_DIGITAL_SIGN_CERT_PVK_INFO</a> structure pointed to by the <b>pSigningCertPvkInfo</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
The certificates in the My store are used.

</td>
</tr>
</table>

### -field pSigningCertContext

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that contains the <a href="/windows/desktop/SecGloss/c-gly">certificate</a> to use to sign the entity. This member is used if <b>CRYPTUI_WIZ_DIGITAL_SIGN_CERT</b> is specified for the <b>dwSigningCertChoice</b> member.

### -field pSigningCertStore

A pointer to a <a href="/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_store_info">CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO</a> structure that contains the certificate to use to sign the entity. This member is used if <b>CRYPTUI_WIZ_DIGITAL_SIGN_STORE</b> is specified for the <b>dwSigningCertChoice</b> member.

### -field pSigningCertPvkInfo

A pointer to a <a href="/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_cert_pvk_info">CRYPTUI_WIZ_DIGITAL_SIGN_CERT_PVK_INFO</a> structure that contains the certificate to use to sign the entity. This member is used if <b>CRYPTUI_WIZ_DIGITAL_SIGN_PVK</b> is specified for the <b>dwSigningCertChoice</b> member.

### -field pwszTimestampURL

A pointer to a null-terminated Unicode string that contains the URL for the time stamp.

### -field dwAdditionalCertChoice

A value that indicates whether additional certificates will be included in the signature. The default value is zero. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_DIGITAL_SIGN_ADD_CHAIN"></a><a id="cryptui_wiz_digital_sign_add_chain"></a><dl>
<dt><b>CRYPTUI_WIZ_DIGITAL_SIGN_ADD_CHAIN</b></dt>
</dl>
</td>
<td width="60%">
The entire certificate  chain will be included in the signature.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_DIGITAL_SIGN_ADD_CHAIN_NO_ROOT"></a><a id="cryptui_wiz_digital_sign_add_chain_no_root"></a><dl>
<dt><b>CRYPTUI_WIZ_DIGITAL_SIGN_ADD_CHAIN_NO_ROOT</b></dt>
</dl>
</td>
<td width="60%">
All certificates in the certificate  chain except the root will be included in the signature.

</td>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
No additional certificates will be included in the signature.

</td>
</tr>
</table>

### -field pSignExtInfo

A pointer to a <a href="/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_extended_info">CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO</a> structure that contains extended information about the signature.

## -see-also

<a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuiwizdigitalsign">CryptUIWizDigitalSign</a>