---
UID: NF:ncrypt.NCryptImportKey
title: NCryptImportKey function
author: windows-sdk-content
description: Imports a Cryptography API:\_Next Generation (CNG) key from a memory BLOB.
old-location: security\ncryptimportkey_func.htm
tech.root: seccng
ms.assetid: ede0e7e0-cb2c-44c0-b724-58db3480b781
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: NCRYPT_SILENT_FLAG, NCryptImportKey, NCryptImportKey function [Security], ncrypt/NCryptImportKey, security.ncryptimportkey_func
ms.topic: function
req.header: ncrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ncrypt.dll
api_name:
 - NCryptImportKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NCryptImportKey function


## -description


The <b>NCryptImportKey</b> function imports a Cryptography API: Next Generation (CNG) key from a memory <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a>.


## -parameters




### -param hProvider [in]

The handle of the key storage provider.


### -param hImportKey [in, optional]

The handle of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic key</a> with which the key data within the imported <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key BLOB</a> was encrypted. This must be a handle to the same key that was passed in the <i>hExportKey</i> parameter of the <a href="https://msdn.microsoft.com/1588eb29-4026-4d1c-8bee-a035df38444a">NCryptExportKey</a> function. If this parameter is <b>NULL</b>, the key BLOB is assumed to not be encrypted.


### -param pszBlobType [in]

A null-terminated Unicode string that contains an identifier that specifies the format of the key BLOB. These formats are specific to a particular key storage provider. For the BLOB formats supported by Microsoft providers, see Remarks.


### -param pParameterList [in, optional]

The address of an <a href="https://msdn.microsoft.com/ae4673ab-81cd-4604-bafa-8d8c66003aba">NCryptBufferDesc</a> structure that points to an array of buffers that contain parameter information for the key.


### -param phKey [out]

The address of an <b>NCRYPT_KEY_HANDLE</b> variable that receives the handle of the key. When you have finished using this handle, release it by passing it to the <a href="https://msdn.microsoft.com/a5535cf9-ba8c-4212-badd-f1dc88903624">NCryptFreeObject</a> function.


### -param pbData [in]

The address of a buffer that contains the key BLOB to be imported. The <i>cbData</i> parameter contains the size of this buffer. 


### -param cbData [in]

The size, in bytes, of the <i>pbData</i> buffer.


### -param dwFlags [in]

Flags that modify function behavior. This can be zero or a combination of one or more of the following values.  The set of valid flags is specific to each key storage provider.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SILENT_FLAG"></a><a id="ncrypt_silent_flag"></a><dl>
<dt><b>NCRYPT_SILENT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Requests that the key service provider (KSP) not display any user interface. If the provider must display the UI to operate, the call fails and the KSP should set the <b>NTE_SILENT_CONTEXT</b> error code as the last error.

</td>
</tr>
</table>
 


## -returns



Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter contains a value that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
A key with the specified name already exists and the <b>NCRYPT_OVERWRITE_KEY_FLAG</b> was not specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hProvider</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -remarks



A service must not call this function from its <a href="http://go.microsoft.com/fwlink/p/?linkid=137250">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.

The following sections describe behaviors specific to the Microsoft key storage providers:

<ul>
<li><b>Microsoft Software KSP</b></li>
<li><b>Microsoft Smart Card KSP</b></li>
</ul>
<h3><a id="microsoft_software_ksp"></a><a id="MICROSOFT_SOFTWARE_KSP"></a>Microsoft Software KSP</h3>
The following constants are supported by the Microsoft software KSP for the <i>pszBlobType</i> parameter.



If a key name is not supplied, the Microsoft Software KSP treats the key as ephemeral and does not store it persistently. For the <b>NCRYPT_OPAQUETRANSPORT_BLOB</b> type, the key name is stored within the BLOB when it is exported. For other BLOB formats, the name can be supplied in an <b> NCRYPTBUFFER_PKCS_KEY_NAME</b> buffer parameter within the <i>pParameterList</i> parameter. 

On Windows Server 2008 and Windows Vista,  only keys imported as PKCS #7 envelope BLOBs (<b>NCRYPT_PKCS7_ENVELOPE_BLOB</b>) or PKCS #8 private key BLOBs (<b>NCRYPT_PKCS8_PRIVATE_KEY_BLOB</b>) can be persisted by using the above method. To persist keys imported through other BLOB types on these platforms, use the method documented in <a href="https://msdn.microsoft.com/37bda1e0-5dd2-455c-9627-4e7e1b0e04d3">Key Import and Export</a>.

The following flags are supported by this KSP.



<table>
<tr>
<th>Term</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="NCRYPT_NO_KEY_VALIDATION"></a><a id="ncrypt_no_key_validation"></a>NCRYPT_NO_KEY_VALIDATION

</td>
<td width="60%">
Do not validate the public portion of the key pair. This flag only 
    applies to public/private key pairs.

</td>
</tr>
<tr>
<td width="40%">
<a id="NCRYPT_DO_NOT_FINALIZE_FLAG"></a><a id="ncrypt_do_not_finalize_flag"></a>NCRYPT_DO_NOT_FINALIZE_FLAG

</td>
<td width="60%">
Do not finalize the key. This option is useful when you need to add or modify properties of the key after importing it. You must finalize the key before it can be used by passing the key handle to the <a href="https://msdn.microsoft.com/4386030d-4ce6-4b2e-adc5-a15ddc869349">NCryptFinalizeKey</a> function. This flag is supported for the private keys PKCS #7 and PKCS #8 but not public keys.

</td>
</tr>
<tr>
<td width="40%">
<a id="NCRYPT_MACHINE_KEY_FLAG"></a><a id="ncrypt_machine_key_flag"></a>NCRYPT_MACHINE_KEY_FLAG

</td>
<td width="60%">
The key applies to the local computer. If this flag is not present, the key applies to the current user.

</td>
</tr>
<tr>
<td width="40%">
<a id="NCRYPT_OVERWRITE_KEY_FLAG"></a><a id="ncrypt_overwrite_key_flag"></a>NCRYPT_OVERWRITE_KEY_FLAG

</td>
<td width="60%">
If a key already exists in the container with the specified name, the existing key will be overwritten. If this flag is not specified and a key with the specified name already exists, this function will return <b>NTE_EXISTS</b>.

</td>
</tr>
<tr>
<td width="40%">
<a id="NCRYPT_WRITE_KEY_TO_LEGACY_STORE_FLAG"></a><a id="ncrypt_write_key_to_legacy_store_flag"></a>NCRYPT_WRITE_KEY_TO_LEGACY_STORE_FLAG

</td>
<td width="60%">
Also save the key in legacy storage. This allows the key to be used with the CryptoAPI. This flag only applies to RSA keys.

</td>
</tr>
</table>
 

<h3><a id="microsoft_smart_card_ksp"></a><a id="MICROSOFT_SMART_CARD_KSP"></a>Microsoft Smart Card KSP</h3>
The set of key BLOB formats and flags supported by this KSP is identical to the set supported by the Microsoft Software KSP.

On Windows Server 2008 and Windows Vista, the Microsoft Smart Card KSP imports all keys into the Microsoft Software KSP. Thus, keys cannot be persisted on to a smart card by using this API, and the guidance in the above section applies when trying to persist keys within the Microsoft Software KSP.

On Windows Server 2008 R2 and Windows 7, the Microsoft Smart Card Key Storage Provider can import a private key to a smart card, provided the following conditions are met:<ul>
<li>The key container name on the card is valid.</li>
<li>Importing private keys is supported by the smart card.</li>
<li>The following two registry keys are set to a <b>DWORD</b> of 0x1:<ul>
<li>
<b>HKLM</b>\<b>SOFTWARE</b>\<b>Microsoft</b>\<b>Cryptography</b>\<b>Defaults</b>\<b>Provider</b>\<b>Microsoft Base Smart Card Crypto Provider</b>\<b>AllowPrivateExchangeKeyImport</b>

</li>
<li>
<b>HKLM</b>\<b>SOFTWARE</b>\<b>Microsoft</b>\<b>Cryptography</b>\<b>Defaults</b>\<b>Provider</b>\<b>Microsoft Base Smart Card Crypto Provider</b>\<b>AllowPrivateSignatureKeyImport</b>

</li>
</ul>
</li>
</ul>


If the key container name is <b>NULL</b>, the Microsoft Smart Card KSP treats the key as ephemeral and imports it into the Microsoft Software KSP.




## -see-also




<a href="https://msdn.microsoft.com/474d3c0d-ae14-448a-a56d-25abc7e5de88">NCryptBuffer</a>
 

 

