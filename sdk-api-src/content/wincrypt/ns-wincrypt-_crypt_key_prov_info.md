---
UID: NS:wincrypt._CRYPT_KEY_PROV_INFO
title: "_CRYPT_KEY_PROV_INFO"
author: windows-sdk-content
description: The CRYPT_KEY_PROV_INFO structure contains information about a key container within a cryptographic service provider (CSP).
old-location: security\crypt_key_prov_info.htm
tech.root: seccrypto
ms.assetid: 6aea2f47-9d4a-4069-ac6d-f28907df00be
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "*PCRYPT_KEY_PROV_INFO, AT_KEYEXCHANGE, AT_SIGNATURE, CERT_SET_KEY_PROV_HANDLE_PROP_ID / CERT_SET_KEY_CONTEXT_PROP_ID, CRYPT_KEY_PROV_INFO, CRYPT_KEY_PROV_INFO structure [Security], CRYPT_MACHINE_KEYSET / NCRYPT_MACHINE_KEY_FLAG, CRYPT_SILENT / NCRYPT_SILENT_FLAG, PCRYPT_KEY_PROV_INFO, PCRYPT_KEY_PROV_INFO structure pointer [Security], _CRYPT_KEY_PROV_INFO, _crypto2_crypt_key_prov_info, security.crypt_key_prov_info, wincrypt/CRYPT_KEY_PROV_INFO, wincrypt/PCRYPT_KEY_PROV_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_KEY_PROV_INFO
product: Windows
targetos: Windows
req.typenames: CRYPT_KEY_PROV_INFO, *PCRYPT_KEY_PROV_INFO
req.redist: 
---

# _CRYPT_KEY_PROV_INFO structure


## -description


The <b>CRYPT_KEY_PROV_INFO</b> structure contains information about a <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key container</a> within a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP).


## -struct-fields




### -field pwszContainerName

A pointer to a null-terminated Unicode string that contains the name of the key container.

When the <b>dwProvType</b> member is zero, this string contains the name of a key within a CNG key storage provider. This string is passed as the <i>pwszKeyName</i> parameter to the <a href="https://msdn.microsoft.com/581c5d89-730d-4d8c-b3bb-a28edec25910">NCryptOpenKey</a> function.


### -field pwszProvName

A pointer to a null-terminated Unicode string that contains the name of the CSP.

When the <b>dwProvType</b> member is zero, this string contains the name of a CNG key storage provider. This string is passed as the <i>pwszProviderName</i> parameter to the <a href="https://msdn.microsoft.com/febcf440-78b3-420b-b13d-030e8071cd50">NCryptOpenStorageProvider</a> function.


### -field dwProvType

Specifies the CSP type. This can be zero or one of the <a href="https://msdn.microsoft.com/ec50d6f1-999d-4ce9-85b4-816afb17550e">Cryptographic Provider Types</a>. 


If this member is zero, the key container is one of the CNG key storage providers.


### -field dwFlags

A set of flags that indicate additional information about the provider. This can be zero or one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_SET_KEY_PROV_HANDLE_PROP_ID___CERT_SET_KEY_CONTEXT_PROP_ID"></a><a id="cert_set_key_prov_handle_prop_id___cert_set_key_context_prop_id"></a><dl>
<dt><b>CERT_SET_KEY_PROV_HANDLE_PROP_ID / CERT_SET_KEY_CONTEXT_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Enables the handle to the key provider to be kept open for subsequent calls to the cryptographic functions.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_MACHINE_KEYSET___NCRYPT_MACHINE_KEY_FLAG"></a><a id="crypt_machine_keyset___ncrypt_machine_key_flag"></a><dl>
<dt><b>CRYPT_MACHINE_KEYSET / NCRYPT_MACHINE_KEY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The key container contains machine keys. If this flag is not present, the key container contains user keys.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_SILENT___NCRYPT_SILENT_FLAG"></a><a id="crypt_silent___ncrypt_silent_flag"></a><dl>
<dt><b>CRYPT_SILENT / NCRYPT_SILENT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The key container will attempt to open any keys silently without any user interface prompts.

</td>
</tr>
</table>
 

The cryptographic functions 
<a href="https://msdn.microsoft.com/e540b816-64e1-4c78-9020-2b221e813acc">CryptDecryptMessage</a>, 
<a href="https://msdn.microsoft.com/f14f7c7b-14ac-40a7-9a49-d1a899ecc52a">CryptSignMessage</a>, 
<a href="https://msdn.microsoft.com/0864a187-617f-4a21-9809-d2dbbc54ab9c">CryptDecryptAndVerifyMessageSignature</a>, and 
<a href="https://msdn.microsoft.com/0ab234f2-a681-463f-8ba8-b23b05cf2626">CryptSignAndEncryptMessage</a> internally perform <a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a> operations using the <b>CRYPT_KEY_PROV_INFO</b> from a certificate. When the <b>CERT_SET_KEY_CONTEXT_PROP_ID</b> or <b>CERT_SET_KEY_PROV_HANDLE_PROP_ID</b> flag is set, these cryptographic functions then can call 
<a href="https://msdn.microsoft.com/b4a0c66d-997f-49cb-935a-9187320037f1">CertSetCertificateContextProperty</a> with <b>CERT_KEY_CONTEXT_PROP_ID</b>. This call enables the handle to the key provider to be kept open for subsequent calls to the cryptographic functions mentioned that use that same certificate, which eliminates the need to perform additional calls to <b>CryptAcquireContext</b>, improving efficiency. Also, because some providers can require that a password be entered for calls to <b>CryptAcquireContext</b>, it is desirable for applications to minimize the number of <b>CryptAcquireContext</b> calls made. Handles to key providers that were kept open are automatically released when the store is closed.
						

For example, consider an email application where five encrypted messages have been received, all encrypted with the public key from the same certificate. If the handle to the key provider is kept open after the first message is processed, calls to 
<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a> are not required for the four remaining messages.


### -field cProvParam

The number of elements in the <b>rgProvParam</b> array.

When the <b>dwProvType</b> member is zero, this member is not used and must be zero.


### -field rgProvParam

An array of <a href="https://msdn.microsoft.com/3731708f-0ce9-42bf-ace9-5ed671be113a">CRYPT_KEY_PROV_PARAM</a> structures that contain the parameters for the key container. The <b>cProvParam</b> member contains the number of elements in this array.

When the <b>dwProvType</b> member is zero, this member is not used and must be <b>NULL</b>.


### -field dwKeySpec

The specification of the private key to retrieve. 


The following values are defined for the default provider.
						

When the <b>dwProvType</b> member is zero, this value is passed as the <i>dwLegacyKeySpec</i> parameter to the <a href="https://msdn.microsoft.com/581c5d89-730d-4d8c-b3bb-a28edec25910">NCryptOpenKey</a> function.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AT_KEYEXCHANGE"></a><a id="at_keyexchange"></a><dl>
<dt><b>AT_KEYEXCHANGE</b></dt>
</dl>
</td>
<td width="60%">
Keys used to encrypt/decrypt session keys.

</td>
</tr>
<tr>
<td width="40%"><a id="AT_SIGNATURE"></a><a id="at_signature"></a><dl>
<dt><b>AT_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
Keys used to create and verify digital signatures.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/3731708f-0ce9-42bf-ace9-5ed671be113a">CRYPT_KEY_PROV_PARAM</a>



<a href="https://msdn.microsoft.com/f766db64-3121-4f70-ac83-ce25ee634efa">CertGetCertificateContextProperty</a>



<a href="https://msdn.microsoft.com/b4a0c66d-997f-49cb-935a-9187320037f1">CertSetCertificateContextProperty</a>
 

 

