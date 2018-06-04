---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# _CRYPTUI_WIZ_IMPORT_SUBJECT_INFO structure


## -description


<p class="CCE_Message">[The  <b>CRYPTUI_WIZ_IMPORT_SRC_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPTUI_WIZ_IMPORT_SRC_INFO</b> structure contains the subject to import into the <a href="https://msdn.microsoft.com/6b2b9c89-229a-4626-a8b4-fe2b7cc0af86">CryptUIWizImport</a> function.  The subject can be a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a>, a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL), or a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL).


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

A pointer to the <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure that contains the certificate to import. This member is used if the <b>dwSubjectChoice</b> member contains <b>CRYPTUI_WIZ_IMPORT_SUBJECT_CERT_CONTEXT</b>.


### -field pCTLContext

A pointer to the <a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a> structure that contains the CTL to import. This member is used if the <b>dwSubjectChoice</b> member contains <b>CRYPTUI_WIZ_IMPORT_SUBJECT_CTL_CONTEXT</b>.


### -field pCRLContext

A pointer to the <a href="https://msdn.microsoft.com/cf7cabcd-b469-492a-b855-8870465ea1cc">CRL_CONTEXT</a> structure that contains the CRL to import. This member is used if the <b>dwSubjectChoice</b> member contains <b>CRYPTUI_WIZ_IMPORT_SUBJECT_CRL_CONTEXT</b>.


### -field hCertStore

A handle to the certificate store to import. This member is used if the <b>dwSubjectChoice</b> member contains <b>CRYPTUI_WIZ_IMPORT_SUBJECT_CERT_STORE</b>.


### -field dwFlags

Contains flags that modify the import operation. This member is required if <b>pwszFileName</b> contains a Personal Information Exchange (PFX) <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a>.  Otherwise, this member is ignored. This member can be zero or a combination of one or more of the following values.

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
the <a href="https://msdn.microsoft.com/8a7c7b46-3bea-4043-b568-6d91d6335737">CryptExportKey</a> function with the key handle fail.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_USER_PROTECTED"></a><a id="crypt_user_protected"></a><dl>
<dt><b>CRYPT_USER_PROTECTED</b></dt>
</dl>
</td>
<td width="60%">
The user is to be notified by means of a dialog box or some other manner when certain actions are attempting to use this key. The precise behavior is specified by the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) that is being used.

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

Pointer to a null-terminated Unicode string that contains the password used to access the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>.  A password is required if <b>pwszFileName</b> contains a PFX BLOB.  If a password is not required, the variable can be an empty string. This member cannot be <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/3c509bb6-d391-4b59-809c-23466c8196ea">CRYPTUI_WIZ_EXPORT_INFO</a>



<a href="https://msdn.microsoft.com/62537d51-c761-4180-b857-58c819ea66aa">CryptUIWizExport</a>
 

 

