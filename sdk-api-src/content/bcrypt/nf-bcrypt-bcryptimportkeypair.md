---
UID: NF:bcrypt.BCryptImportKeyPair
title: BCryptImportKeyPair function (bcrypt.h)
author: windows-sdk-content
description: Imports a public/private key pair from a key BLOB.
old-location: security\bcryptimportkeypair.htm
tech.root: seccng
ms.assetid: 271fc084-6121-4666-b521-b849c7d7966c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BCRYPT_DH_PRIVATE_BLOB, BCRYPT_DH_PUBLIC_BLOB, BCRYPT_DSA_PRIVATE_BLOB, BCRYPT_DSA_PUBLIC_BLOB, BCRYPT_ECCPRIVATE_BLOB, BCRYPT_ECCPUBLIC_BLOB, BCRYPT_NO_KEY_VALIDATION, BCRYPT_PRIVATE_KEY_BLOB, BCRYPT_PUBLIC_KEY_BLOB, BCRYPT_RSAPRIVATE_BLOB, BCRYPT_RSAPUBLIC_BLOB, BCryptImportKeyPair, BCryptImportKeyPair function [Security], LEGACY_DH_PRIVATE_BLOB, LEGACY_DH_PUBLIC_BLOB, LEGACY_DSA_PRIVATE_BLOB, LEGACY_DSA_PUBLIC_BLOB, LEGACY_DSA_V2_PRIVATE_BLOB, LEGACY_RSAPRIVATE_BLOB, LEGACY_RSAPUBLIC_BLOB, bcrypt/BCryptImportKeyPair, security.bcryptimportkeypair
ms.topic: function
req.header: bcrypt.h
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
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
 - Ksecdd.sys
api_name:
 - BCryptImportKeyPair
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BCryptImportKeyPair function


## -description


The <b>BCryptImportKeyPair</b> function imports a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public/private key pair</a> from a key <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a>. The <a href="https://msdn.microsoft.com/6b9683f4-10f2-40e4-9757-a1f01991bef7">BCryptImportKey</a> function is used to import a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">symmetric key</a> pair.


## -parameters




### -param hAlgorithm [in]

The handle of the algorithm provider to import the key. This handle is obtained by calling the <a href="https://msdn.microsoft.com/aceba9c0-19e6-4f3c-972a-752feed4a9f8">BCryptOpenAlgorithmProvider</a> function.


### -param hImportKey [in, out]

This parameter is not currently used and should be <b>NULL</b>.


### -param pszBlobType [in]

A null-terminated Unicode string that contains an identifier that specifies the type of BLOB that is contained in the <i>pbInput</i> buffer. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_DH_PRIVATE_BLOB"></a><a id="bcrypt_dh_private_blob"></a><dl>
<dt><b>BCRYPT_DH_PRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a Diffie-Hellman public/private key pair BLOB. The <i>pbInput</i> buffer must contain a <a href="https://msdn.microsoft.com/6004b2e5-7e06-4108-a0da-472b9b6d5fea">BCRYPT_DH_KEY_BLOB</a> structure immediately followed by the key data.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_DH_PUBLIC_BLOB"></a><a id="bcrypt_dh_public_blob"></a><dl>
<dt><b>BCRYPT_DH_PUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a Diffie-Hellman <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key BLOB</a>. The <i>pbInput</i> buffer must contain a <a href="https://msdn.microsoft.com/6004b2e5-7e06-4108-a0da-472b9b6d5fea">BCRYPT_DH_KEY_BLOB</a> structure immediately followed by the key data.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_DSA_PRIVATE_BLOB"></a><a id="bcrypt_dsa_private_blob"></a><dl>
<dt><b>BCRYPT_DSA_PRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a DSA public/private key pair BLOB. The <i>pbInput</i> buffer must contain a <a href="https://msdn.microsoft.com/3db36170-106e-49c8-9866-e25759bdd7f9">BCRYPT_DSA_KEY_BLOB</a> or <a href="https://msdn.microsoft.com/E8240DE1-B65F-4DAC-92C9-45725435A0F7">BCRYPT_DSA_KEY_BLOB_V2</a> structure immediately followed by the key data. <b>BCRYPT_DSA_KEY_BLOB</b> is used for key lengths from 512 to 1024 bits. <b>BCRYPT_DSA_KEY_BLOB_V2</b> is used for key lengths that exceed 1024 bits but are less than or equal to 3072 bits.

<b>Windows 8:  </b>Support for <a href="https://msdn.microsoft.com/E8240DE1-B65F-4DAC-92C9-45725435A0F7">BCRYPT_DSA_KEY_BLOB_V2</a> begins.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_DSA_PUBLIC_BLOB"></a><a id="bcrypt_dsa_public_blob"></a><dl>
<dt><b>BCRYPT_DSA_PUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a DSA public key BLOB. The <i>pbInput</i> buffer must contain a <a href="https://msdn.microsoft.com/3db36170-106e-49c8-9866-e25759bdd7f9">BCRYPT_DSA_KEY_BLOB</a> or <a href="https://msdn.microsoft.com/E8240DE1-B65F-4DAC-92C9-45725435A0F7">BCRYPT_DSA_KEY_BLOB_V2</a> structure immediately followed by the key data. <b>BCRYPT_DSA_KEY_BLOB</b> is used for key lengths from 512 to 1024 bits. <b>BCRYPT_DSA_KEY_BLOB_V2</b> is used for key lengths that exceed 1024 bits but are less than or equal to 3072 bits.

<b>Windows 8:  </b>Support for <a href="https://msdn.microsoft.com/E8240DE1-B65F-4DAC-92C9-45725435A0F7">BCRYPT_DSA_KEY_BLOB_V2</a> begins.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_ECCPRIVATE_BLOB"></a><a id="bcrypt_eccprivate_blob"></a><dl>
<dt><b>BCRYPT_ECCPRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is an <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">elliptic curve cryptography</a> (ECC) <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>. The <i>pbInput</i> buffer must contain a <a href="https://msdn.microsoft.com/e60f6630-e4b0-4f35-a3cf-95dbcb007124">BCRYPT_ECCKEY_BLOB</a> structure immediately followed by the key data. 

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_ECCPUBLIC_BLOB"></a><a id="bcrypt_eccpublic_blob"></a><dl>
<dt><b>BCRYPT_ECCPUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is an ECC public key. The <i>pbInput</i> buffer must contain a <a href="https://msdn.microsoft.com/e60f6630-e4b0-4f35-a3cf-95dbcb007124">BCRYPT_ECCKEY_BLOB</a> structure immediately followed by the key data.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_PUBLIC_KEY_BLOB"></a><a id="bcrypt_public_key_blob"></a><dl>
<dt><b>BCRYPT_PUBLIC_KEY_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a generic <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> of any type. The type of key in this BLOB is determined by the <b>Magic</b> member of the <a href="https://msdn.microsoft.com/ae7e8db3-858d-4573-afe1-c9bc14d76480">BCRYPT_KEY_BLOB</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_PRIVATE_KEY_BLOB"></a><a id="bcrypt_private_key_blob"></a><dl>
<dt><b>BCRYPT_PRIVATE_KEY_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a generic private key of any type. The private key does not necessarily contain the public key. The type of key in this BLOB is determined by the <b>Magic</b> member of the <a href="https://msdn.microsoft.com/ae7e8db3-858d-4573-afe1-c9bc14d76480">BCRYPT_KEY_BLOB</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RSAPRIVATE_BLOB"></a><a id="bcrypt_rsaprivate_blob"></a><dl>
<dt><b>BCRYPT_RSAPRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is an RSA public/private key pair BLOB. The <i>pbInput</i> buffer must contain a <a href="https://msdn.microsoft.com/bbf3f4b9-5c69-4212-bb23-34bb2c84185c">BCRYPT_RSAKEY_BLOB</a> structure immediately followed by the key data.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RSAPUBLIC_BLOB"></a><a id="bcrypt_rsapublic_blob"></a><dl>
<dt><b>BCRYPT_RSAPUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is an RSA public key BLOB. The <i>pbInput</i> buffer must contain a <a href="https://msdn.microsoft.com/bbf3f4b9-5c69-4212-bb23-34bb2c84185c">BCRYPT_RSAKEY_BLOB</a> structure immediately followed by the key data.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_DH_PUBLIC_BLOB"></a><a id="legacy_dh_public_blob"></a><dl>
<dt><b>LEGACY_DH_PUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a Diffie-Hellman public key BLOB that was exported by using <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CryptoAPI</a>. The Microsoft primitive provider does not support importing this BLOB type.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_DH_PRIVATE_BLOB"></a><a id="legacy_dh_private_blob"></a><dl>
<dt><b>LEGACY_DH_PRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a legacy <a href="https://msdn.microsoft.com/c759e6e1-f7af-4cd6-a67e-ff0da1e91eb1">Diffie-Hellman Version 3 Private Key BLOB</a> that contains a Diffie-Hellman public/private key pair that was exported by using CryptoAPI.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_DSA_PRIVATE_BLOB"></a><a id="legacy_dsa_private_blob"></a><dl>
<dt><b>LEGACY_DSA_PRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a DSA public/private key pair BLOB that was exported by using CryptoAPI.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_DSA_PUBLIC_BLOB"></a><a id="legacy_dsa_public_blob"></a><dl>
<dt><b>LEGACY_DSA_PUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a DSA public key BLOB that was exported by using CryptoAPI. The Microsoft primitive provider does not support importing this BLOB type.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_DSA_V2_PRIVATE_BLOB"></a><a id="legacy_dsa_v2_private_blob"></a><dl>
<dt><b>LEGACY_DSA_V2_PRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a DSA version 2 private key in a form that can be imported by using CryptoAPI.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_RSAPRIVATE_BLOB"></a><a id="legacy_rsaprivate_blob"></a><dl>
<dt><b>LEGACY_RSAPRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is an RSA public/private key pair BLOB that was exported by using CryptoAPI.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_RSAPUBLIC_BLOB"></a><a id="legacy_rsapublic_blob"></a><dl>
<dt><b>LEGACY_RSAPUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is an RSA public key BLOB that was exported by using CryptoAPI. The Microsoft primitive provider does not support importing this BLOB type.

</td>
</tr>
</table>
 


### -param phKey [out]

A pointer to a <b>BCRYPT_KEY_HANDLE</b> that receives the handle of the imported key. This handle is used in subsequent functions that require a key, such as <a href="https://msdn.microsoft.com/f402ea9e-89ae-4ccc-9591-aa2328287c0e">BCryptSignHash</a>. This handle must be released when it is no longer needed by passing it to the <a href="https://msdn.microsoft.com/98c02e55-6489-4901-8a7a-021baac41965">BCryptDestroyKey</a> function.


### -param pbInput [in]

The address of a buffer that contains the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key BLOB</a> to import. The <i>cbInput</i> parameter contains the size of this buffer. The <i>pszBlobType</i> parameter specifies the type of key BLOB this buffer contains.


### -param cbInput [in]

The size, in bytes, of the <i>pbInput</i> buffer.


### -param dwFlags [in]

A set of flags that modify the behavior of this function. This can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_NO_KEY_VALIDATION"></a><a id="bcrypt_no_key_validation"></a><dl>
<dt><b>BCRYPT_NO_KEY_VALIDATION</b></dt>
</dl>
</td>
<td width="60%">
Do not validate the public portion of the key pair.

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
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The algorithm handle in the <i>hAlgorithm</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The algorithm provider specified by the <i>hAlgorithm</i> parameter does not support the BLOB type specified by the <i>pszBlobType</i> parameter.

</td>
</tr>
</table>
 




## -remarks



Depending on what processor modes a provider supports, <b>BCryptImportKeyPair</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hAlgorithm</i> parameter must have been opened by using the <b>BCRYPT_PROV_DISPATCH</b> flag, and any pointers passed to the <b>BCryptImportKeyPair</b> function must refer to nonpaged (or locked) memory.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=84080">WDK and Developer Tools</a>.<b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.






## -see-also




<a href="https://msdn.microsoft.com/98c02e55-6489-4901-8a7a-021baac41965">BCryptDestroyKey</a>



<a href="https://msdn.microsoft.com/a5d73143-c1d6-43b3-a724-7e27c68a5ade">BCryptExportKey</a>



<a href="https://msdn.microsoft.com/6b9683f4-10f2-40e4-9757-a1f01991bef7">BCryptImportKey</a>
 

 

