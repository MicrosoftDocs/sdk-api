---
UID: NS:cryptuiapi._CRYPTUI_WIZ_EXPORT_INFO
title: CRYPTUI_WIZ_EXPORT_INFO (cryptuiapi.h)
description: Contains information that controls the operation of the CryptUIWizExport function.
helpviewer_keywords: ["*PCRYPTUI_WIZ_EXPORT_INFO","CRYPTUI_WIZ_EXPORT_CERT_CONTEXT","CRYPTUI_WIZ_EXPORT_CERT_STORE","CRYPTUI_WIZ_EXPORT_CERT_STORE_CERTIFICATES_ONLY","CRYPTUI_WIZ_EXPORT_CRL_CONTEXT","CRYPTUI_WIZ_EXPORT_CTL_CONTEXT","CRYPTUI_WIZ_EXPORT_INFO","CRYPTUI_WIZ_EXPORT_INFO structure [Security]","PCRYPTUI_WIZ_EXPORT_INFO","PCRYPTUI_WIZ_EXPORT_INFO structure pointer [Security]","cryptuiapi/CRYPTUI_WIZ_EXPORT_INFO","cryptuiapi/PCRYPTUI_WIZ_EXPORT_INFO","security.cryptui_wiz_export_info"]
old-location: security\cryptui_wiz_export_info.htm
tech.root: security
ms.assetid: 3c509bb6-d391-4b59-809c-23466c8196ea
ms.date: 12/05/2018
ms.keywords: '*PCRYPTUI_WIZ_EXPORT_INFO, CRYPTUI_WIZ_EXPORT_CERT_CONTEXT, CRYPTUI_WIZ_EXPORT_CERT_STORE, CRYPTUI_WIZ_EXPORT_CERT_STORE_CERTIFICATES_ONLY, CRYPTUI_WIZ_EXPORT_CRL_CONTEXT, CRYPTUI_WIZ_EXPORT_CTL_CONTEXT, CRYPTUI_WIZ_EXPORT_INFO, CRYPTUI_WIZ_EXPORT_INFO structure [Security], PCRYPTUI_WIZ_EXPORT_INFO, PCRYPTUI_WIZ_EXPORT_INFO structure pointer [Security], cryptuiapi/CRYPTUI_WIZ_EXPORT_INFO, cryptuiapi/PCRYPTUI_WIZ_EXPORT_INFO, security.cryptui_wiz_export_info'
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
req.typenames: CRYPTUI_WIZ_EXPORT_INFO, *PCRYPTUI_WIZ_EXPORT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPTUI_WIZ_EXPORT_INFO
 - cryptuiapi/_CRYPTUI_WIZ_EXPORT_INFO
 - PCRYPTUI_WIZ_EXPORT_INFO
 - cryptuiapi/PCRYPTUI_WIZ_EXPORT_INFO
 - CRYPTUI_WIZ_EXPORT_INFO
 - cryptuiapi/CRYPTUI_WIZ_EXPORT_INFO
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
 - CRYPTUI_WIZ_EXPORT_INFO
---

# CRYPTUI_WIZ_EXPORT_INFO structure


## -description

<p class="CCE_Message">[The  <b>CRYPTUI_WIZ_EXPORT_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPTUI_WIZ_EXPORT_INFO</b> structure contains information that controls the operation of the <a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuiwizexport">CryptUIWizExport</a> function.

## -struct-fields

### -field dwSize

The size, in bytes, of this structure.

### -field pwszExportFileName

A pointer to a null-terminated Unicode string that contains the fully qualified file name to export to. If this member is
not <b>NULL</b> and the <b>CRYPTUI_WIZ_NO_UI</b> flag in the <i>dwFlags</i> parameter of the <a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuiwizexport">CryptUIWizExport</a> function is not set, this string is
displayed to the user as the default file name. This member is required if the <b>CRYPTUI_WIZ_NO_UI</b> flag is set.  This member is otherwise optional.

### -field dwSubjectChoice

Indicates the type of the subject to export.  This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_EXPORT_CERT_CONTEXT"></a><a id="cryptui_wiz_export_cert_context"></a><dl>
<dt><b>CRYPTUI_WIZ_EXPORT_CERT_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
Export the certificate context that is specified in the <b>pCertContext</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_EXPORT_CTL_CONTEXT"></a><a id="cryptui_wiz_export_ctl_context"></a><dl>
<dt><b>CRYPTUI_WIZ_EXPORT_CTL_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
Export the <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL) context that is specified in the <b>pCTLContext</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_EXPORT_CRL_CONTEXT"></a><a id="cryptui_wiz_export_crl_context"></a><dl>
<dt><b>CRYPTUI_WIZ_EXPORT_CRL_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
Export the <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) context that is specified in the <b>pCRLContext</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_EXPORT_CERT_STORE"></a><a id="cryptui_wiz_export_cert_store"></a><dl>
<dt><b>CRYPTUI_WIZ_EXPORT_CERT_STORE</b></dt>
</dl>
</td>
<td width="60%">
Export the <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> that is specified in the <b>hCertStore</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_EXPORT_CERT_STORE_CERTIFICATES_ONLY"></a><a id="cryptui_wiz_export_cert_store_certificates_only"></a><dl>
<dt><b>CRYPTUI_WIZ_EXPORT_CERT_STORE_CERTIFICATES_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Export only the <a href="/windows/desktop/SecGloss/c-gly">certificates</a> from the certificate store that is specified in the <b>hCertStore</b> member.

</td>
</tr>
</table>

### -field pCertContext

A pointer to the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that contains the certificate to export. This member is used if the <b>dwSubjectChoice</b> member contains <b>CRYPTUI_WIZ_EXPORT_CERT_CONTEXT</b>.

### -field pCTLContext

A pointer to the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure that contains the CTL to export. This member is used if the <b>dwSubjectChoice</b> member contains <b>CRYPTUI_WIZ_EXPORT_CTL_CONTEXT</b>.

### -field pCRLContext

A pointer to the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> structure that contains the CRL to export. This member is used if the <b>dwSubjectChoice</b> member contains <b>CRYPTUI_WIZ_EXPORT_CRL_CONTEXT</b>.

### -field hCertStore

A handle to the certificate store to export. This member is used if the <b>dwSubjectChoice</b> member contains <b>CRYPTUI_WIZ_EXPORT_CERT_STORE</b> or <b>CRYPTUI_WIZ_EXPORT_CERT_STORE_CERTIFICATES_ONLY</b>.

### -field cStores

The number of elements in the <b>rghStores</b> array.

### -field rghStores

An array of extra certificate stores to search for certificates in the trust chain if the chain is being exported with a certificate.
This member is ignored if <b>dwSubjectChoice</b> is anything other than the   <b>CRYPTUI_WIZ_EXPORT_CERT_CONTEXT</b> value. The <b>cStores</b> member contains the number of elements in this array.

## -see-also

<a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuiwizexport">CryptUIWizExport</a>