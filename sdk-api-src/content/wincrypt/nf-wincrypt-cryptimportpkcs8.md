---
UID: NF:wincrypt.CryptImportPKCS8
title: CryptImportPKCS8 function
author: windows-sdk-content
description: Imports the private key in PKCS #8 format to a cryptographic service provider (CSP).
old-location: security\cryptimportpkcs8.htm
old-project: SecCrypto
ms.assetid: fa3deff9-b4c1-4b63-a59f-738f87e1a409
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: CRYPT_EXPORTABLE, CRYPT_USER_PROTECTED, CryptImportPKCS8, CryptImportPKCS8 function [Security], security.cryptimportpkcs8, wincrypt/CryptImportPKCS8
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
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
tech.root: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptImportPKCS8
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptImportPKCS8 function


## -description


<p class="CCE_Message">[The <b>CryptImportPKCS8</b> function is no longer available for use as of Windows Server 2008 and Windows Vista. Instead, use the <a href="https://msdn.microsoft.com/2c83774a-f2df-4d28-9abd-e39aa507ba88">PFXImportCertStore</a> function.]
<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptImportPKCS8</b> function imports the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> in PKCS #8 format to a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP).<b>CryptImportPKCS8</b> will return a handle to the provider and the import KeySpec used.


## -parameters




### -param sPrivateKeyAndParams [in]

A <a href="https://msdn.microsoft.com/a016e807-60d3-4ae4-829b-43acea2ee8c1">CRYPT_PKCS8_IMPORT_PARAMS</a> structure that contains the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key BLOB</a> and corresponding parameters.


### -param dwFlags [in]

A  <b>DWORD</b>  value. This parameter can be one of the following values, a combination of them, or a null value.

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
The key being imported is eventually to be reexported. If this flag is not used, then calls to 
<a href="https://msdn.microsoft.com/8a7c7b46-3bea-4043-b568-6d91d6335737">CryptExportKey</a> with the key handle fail.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_USER_PROTECTED"></a><a id="crypt_user_protected"></a><dl>
<dt><b>CRYPT_USER_PROTECTED</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the CSP notifies the user through a dialog box or some other method when certain actions are attempted using this key. The precise behavior is specified by the CSP or the CSP type used. 
If the provider context was acquired with CRYPT_SILENT set, using this flag causes a failure, and the last error is set to NTE_SILENT_CONTEXT.

</td>
</tr>
</table>
 


### -param phCryptProv [out, optional]

A pointer to the <a href="https://msdn.microsoft.com/8ec6b392-06bc-4717-8657-7ea9a43d03fb">HCRYPTPROV</a>  to receive the handle of the provider into which the key is
imported by calling the <b>CryptImportPKCS8</b> function.  

When you have finished using the handle, free the handle by calling <a href="https://msdn.microsoft.com/c1e3e708-b543-4e87-8638-a9946a83e614">CryptReleaseContext</a>. 

This parameter can be <b>NULL</b>, in which case the handle of the provider is not returned.


### -param pvAuxInfo [in, optional]

This parameter must be <b>NULL</b>.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following error code is specific to this function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNSUPPORTED_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The algorithm <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) of the private
      key is not supported.

</td>
</tr>
</table>
 

If the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>  may return an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="https://msdn.microsoft.com/cb1f34dd-dab4-4ffb-a73b-79a214290509">ASN.1 Encoding/Decoding Return Values</a>.




## -remarks



<b>CryptImportPKCS8</b>  calls the <a href="https://msdn.microsoft.com/d3b2b942-bde5-4399-9412-95fe227cd546">PCRYPT_RESOLVE_HCRYPTPROV_FUNC</a> function  by using the <a href="https://msdn.microsoft.com/a016e807-60d3-4ae4-829b-43acea2ee8c1">CRYPT_PKCS8_IMPORT_PARAMS</a> structure contained in the <i>sPrivateKeyAndParams</i> parameter to retrieve a handle of the provider to which to import the key.  If  <b>PCRYPT_RESOLVE_HCRYPTPROV_FUNC</b> is <b>NULL</b>, then the default provider is used.

This function is only supported for asymmetric keys.




## -see-also




<a href="https://msdn.microsoft.com/a016e807-60d3-4ae4-829b-43acea2ee8c1">CRYPT_PKCS8_IMPORT_PARAMS</a>



<a href="https://msdn.microsoft.com/82fee86a-8704-4f22-8f11-f89509c5a0aa">CryptExportPKCS8Ex</a>



<a href="https://msdn.microsoft.com/c1e3e708-b543-4e87-8638-a9946a83e614">CryptReleaseContext</a>



<a href="https://msdn.microsoft.com/f59fd46b-5430-4aa2-85ba-961b416dbaac">PCRYPT_DECRYPT_PRIVATE_KEY_FUNC</a>



<a href="https://msdn.microsoft.com/d3b2b942-bde5-4399-9412-95fe227cd546">PCRYPT_RESOLVE_HCRYPTPROV_FUNC</a>
 

 

