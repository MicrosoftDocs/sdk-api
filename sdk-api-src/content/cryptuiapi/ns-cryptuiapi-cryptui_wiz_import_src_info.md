---
UID: NS:cryptuiapi._CRYPTUI_WIZ_IMPORT_SUBJECT_INFO
title: CRYPTUI_WIZ_IMPORT_SRC_INFO (cryptuiapi.h)
description: Contains the subject to import into the CryptUIWizImport function.
helpviewer_keywords: ["*PCRYPTUI_WIZ_IMPORT_SRC_INFO","CRYPTUI_WIZ_IMPORT_SRC_INFO","CRYPTUI_WIZ_IMPORT_SRC_INFO structure [Security]","CRYPTUI_WIZ_IMPORT_SUBJECT_CERT_CONTEXT","CRYPTUI_WIZ_IMPORT_SUBJECT_CERT_STORE","CRYPTUI_WIZ_IMPORT_SUBJECT_CRL_CONTEXT","CRYPTUI_WIZ_IMPORT_SUBJECT_CTL_CONTEXT","CRYPTUI_WIZ_IMPORT_SUBJECT_FILE","CRYPT_EXPORTABLE","CRYPT_MACHINE_KEYSET","CRYPT_USER_KEYSET","CRYPT_USER_PROTECTED","PCCRYPTUI_WIZ_IMPORT_SRC_INFO","PCCRYPTUI_WIZ_IMPORT_SRC_INFO structure pointer [Security]","cryptuiapi/CRYPTUI_WIZ_IMPORT_SRC_INFO","cryptuiapi/PCCRYPTUI_WIZ_IMPORT_SRC_INFO","security.cryptui_wiz_import_src_info"]
old-location: security\cryptui_wiz_import_src_info.htm
tech.root: security
ms.assetid: 17d932e3-05ea-4ed0-9f88-fbb674b6b070
ms.date: 12/05/2018
ms.keywords: '*PCRYPTUI_WIZ_IMPORT_SRC_INFO, CRYPTUI_WIZ_IMPORT_SRC_INFO, CRYPTUI_WIZ_IMPORT_SRC_INFO structure [Security], CRYPTUI_WIZ_IMPORT_SUBJECT_CERT_CONTEXT, CRYPTUI_WIZ_IMPORT_SUBJECT_CERT_STORE, CRYPTUI_WIZ_IMPORT_SUBJECT_CRL_CONTEXT, CRYPTUI_WIZ_IMPORT_SUBJECT_CTL_CONTEXT, CRYPTUI_WIZ_IMPORT_SUBJECT_FILE, CRYPT_EXPORTABLE, CRYPT_MACHINE_KEYSET, CRYPT_USER_KEYSET, CRYPT_USER_PROTECTED, PCCRYPTUI_WIZ_IMPORT_SRC_INFO, PCCRYPTUI_WIZ_IMPORT_SRC_INFO structure pointer [Security], cryptuiapi/CRYPTUI_WIZ_IMPORT_SRC_INFO, cryptuiapi/PCCRYPTUI_WIZ_IMPORT_SRC_INFO, security.cryptui_wiz_import_src_info'
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
req.typenames: CRYPTUI_WIZ_IMPORT_SRC_INFO, *PCRYPTUI_WIZ_IMPORT_SRC_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPTUI_WIZ_IMPORT_SUBJECT_INFO
 - cryptuiapi/_CRYPTUI_WIZ_IMPORT_SUBJECT_INFO
 - PCRYPTUI_WIZ_IMPORT_SRC_INFO
 - cryptuiapi/PCRYPTUI_WIZ_IMPORT_SRC_INFO
 - CRYPTUI_WIZ_IMPORT_SRC_INFO
 - cryptuiapi/CRYPTUI_WIZ_IMPORT_SRC_INFO
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
 - CRYPTUI_WIZ_IMPORT_SRC_INFO
---

# CRYPTUI_WIZ_IMPORT_SRC_INFO structure


## -description

<p class="CCE_Message">[The  <b>CRYPTUI_WIZ_IMPORT_SRC_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPTUI_WIZ_IMPORT_SRC_INFO</b> structure contains the subject to import into the <a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuiwizimport">CryptUIWizImport</a> function.  The subject can be a <a href="/windows/desktop/SecGloss/c-gly">certificate</a>, a <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL), or a <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL).

## -struct-fields

### -field dwSize

The size, in bytes, of this structure.

### -field dwSubjectChoice

Indicates the type of subject to import.  This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_IMPORT_SUBJECT_FILE"></a><a id="cryptui_wiz_import_subject_file"></a><dl>
<dt><b>CRYPTUI_WIZ_IMPORT_SUBJECT_FILE</b></dt>
</dl>
</td>
<td width="60%">
Import the certificate stored in the file referenced in the <b>pwszFileName</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_IMPORT_SUBJECT_CERT_CONTEXT"></a><a id="cryptui_wiz_import_subject_cert_context"></a><dl>
<dt><b>CRYPTUI_WIZ_IMPORT_SUBJECT_CERT_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
Import the certificate referenced in the <b>pCertContext</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_IMPORT_SUBJECT_CTL_CONTEXT"></a><a id="cryptui_wiz_import_subject_ctl_context"></a><dl>
<dt><b>CRYPTUI_WIZ_IMPORT_SUBJECT_CTL_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
Import the CTL referenced in the <b>pCTLContext</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_IMPORT_SUBJECT_CRL_CONTEXT"></a><a id="cryptui_wiz_import_subject_crl_context"></a><dl>
<dt><b>CRYPTUI_WIZ_IMPORT_SUBJECT_CRL_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
Import the CRL referenced in the <b>pCRLContext</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_IMPORT_SUBJECT_CERT_STORE"></a><a id="cryptui_wiz_import_subject_cert_store"></a><dl>
<dt><b>CRYPTUI_WIZ_IMPORT_SUBJECT_CERT_STORE</b></dt>
</dl>
</td>
<td width="60%">
Import the certificate store referenced in the <b>hCertStore</b> member.

</td>
</tr>
</table>

### -field pwszFileName

A pointer to a null-terminated Unicode string that contains the path and file name of the file that contains the certificate to import. This member is used if the <b>dwSubjectChoice</b> member contains <b>CRYPTUI_WIZ_IMPORT_SUBJECT_FILE</b>.

### -field pCertContext

A pointer to the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that contains the certificate to import. This member is used if the <b>dwSubjectChoice</b> member contains <b>CRYPTUI_WIZ_IMPORT_SUBJECT_CERT_CONTEXT</b>.

### -field pCTLContext

A pointer to the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure that contains the CTL to import. This member is used if the <b>dwSubjectChoice</b> member contains <b>CRYPTUI_WIZ_IMPORT_SUBJECT_CTL_CONTEXT</b>.

### -field pCRLContext

A pointer to the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> structure that contains the CRL to import. This member is used if the <b>dwSubjectChoice</b> member contains <b>CRYPTUI_WIZ_IMPORT_SUBJECT_CRL_CONTEXT</b>.

### -field hCertStore

A handle to the certificate store to import. This member is used if the <b>dwSubjectChoice</b> member contains <b>CRYPTUI_WIZ_IMPORT_SUBJECT_CERT_STORE</b>.

### -field dwFlags

Contains flags that modify the import operation. This member is required if <b>pwszFileName</b> contains a Personal Information Exchange (PFX) <a href="/windows/desktop/SecGloss/b-gly">BLOB</a>.  Otherwise, this member is ignored. This member can be zero or a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_EXPORTABLE"></a><a id="crypt_exportable"></a><dl>
<dt><b>CRYPT_EXPORTABLE</b></dt>
</dl>
</td>
<td width="60%">
Imported keys are marked as exportable. If this flag is not used, calls to 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportkey">CryptExportKey</a> function with the key handle fail.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_USER_PROTECTED"></a><a id="crypt_user_protected"></a><dl>
<dt><b>CRYPT_USER_PROTECTED</b></dt>
</dl>
</td>
<td width="60%">
The user is to be notified by means of a dialog box or some other manner when certain actions are attempting to use this key. The precise behavior is specified by the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) that is being used.

Prior to Internet Explorer 4.0, Microsoft CSPs ignored this flag. Starting with Internet Explorer 4.0, Microsoft CSPs support this flag.

If the provider context was opened with the <b>CRYPT_SILENT</b> flag set, using this flag causes a failure, and the last error is set to <b>NTE_SILENT_CONTEXT</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_MACHINE_KEYSET"></a><a id="crypt_machine_keyset"></a><dl>
<dt><b>CRYPT_MACHINE_KEYSET</b></dt>
</dl>
</td>
<td width="60%">
The private keys are stored under the local computer and not under the current user.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_USER_KEYSET"></a><a id="crypt_user_keyset"></a><dl>
<dt><b>CRYPT_USER_KEYSET</b></dt>
</dl>
</td>
<td width="60%">
The private keys are stored under the current user and not under the local computer, even if the PFX BLOB specifies that they should go under the local computer.

</td>
</tr>
</table>

### -field pwszPassword

Pointer to a null-terminated Unicode string that contains the password used to access the <a href="/windows/desktop/SecGloss/p-gly">private key</a>.  A password is required if <b>pwszFileName</b> contains a PFX BLOB.  If a password is not required, the variable can be an empty string. This member cannot be <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_export_info">CRYPTUI_WIZ_EXPORT_INFO</a>



<a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuiwizexport">CryptUIWizExport</a>