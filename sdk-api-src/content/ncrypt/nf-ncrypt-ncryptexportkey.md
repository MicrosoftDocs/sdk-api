---
UID: NF:ncrypt.NCryptExportKey
title: NCryptExportKey function
author: windows-driver-content
description: Exports a CNG key to a memory BLOB.
old-location: security\ncryptexportkey_func.htm
old-project: SecCNG
ms.assetid: 1588eb29-4026-4d1c-8bee-a035df38444a
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: BCRYPT_DH_PRIVATE_BLOB, BCRYPT_DH_PUBLIC_BLOB, BCRYPT_DSA_PRIVATE_BLOB, BCRYPT_DSA_PUBLIC_BLOB, BCRYPT_ECCPRIVATE_BLOB, BCRYPT_ECCPUBLIC_BLOB, BCRYPT_PRIVATE_KEY_BLOB, BCRYPT_PUBLIC_KEY_BLOB, BCRYPT_RSAFULLPRIVATE_BLOB, BCRYPT_RSAPRIVATE_BLOB, BCRYPT_RSAPUBLIC_BLOB, LEGACY_DH_PRIVATE_BLOB, LEGACY_DH_PUBLIC_BLOB, LEGACY_DSA_PRIVATE_BLOB, LEGACY_DSA_PUBLIC_BLOB, LEGACY_RSAPRIVATE_BLOB, LEGACY_RSAPUBLIC_BLOB, NCRYPT_CIPHER_KEY_BLOB, NCRYPT_OPAQUETRANSPORT_BLOB, NCRYPT_PKCS7_ENVELOPE_BLOB, NCRYPT_PKCS8_PRIVATE_KEY_BLOB, NCRYPT_PROTECTED_KEY_BLOB, NCRYPT_SILENT_FLAG, NCryptExportKey, NCryptExportKey function [Security], ncrypt/NCryptExportKey, security.ncryptexportkey_func
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ncrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SESSION_HEADER, *PSESSION_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ncrypt.dll
api_name:
-	NCryptExportKey
product: Windows
targetos: Windows
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# NCryptExportKey function


## -description


The <b>NCryptExportKey</b> function exports a CNG key to a memory <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a>.


## -parameters




### -param hKey [in]

A handle of the key to export.


### -param hExportKey [in, optional]

A handle to a cryptographic key of the destination user. The key data within the exported key BLOB is encrypted by using this key. This ensures that only the destination user is able to make use of the key BLOB.


### -param pszBlobType [in]

A null-terminated Unicode string that contains an identifier that specifies the type of BLOB to export. This can be one of the following values.



#### BCRYPT_DH_PRIVATE_BLOB

Export a Diffie-Hellman <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public/private key pair</a>. The <i>pbOutput</i> buffer receives a <a href="https://msdn.microsoft.com/6004b2e5-7e06-4108-a0da-472b9b6d5fea">BCRYPT_DH_KEY_BLOB</a> structure immediately followed by the key data.



#### BCRYPT_DH_PUBLIC_BLOB

Export a Diffie-Hellman <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a>. The <i>pbOutput</i> buffer receives a <a href="https://msdn.microsoft.com/6004b2e5-7e06-4108-a0da-472b9b6d5fea">BCRYPT_DH_KEY_BLOB</a> structure immediately followed by the key data.



#### BCRYPT_DSA_PRIVATE_BLOB

Export a DSA public/private key pair. The <i>pbOutput</i> buffer receives a <a href="https://msdn.microsoft.com/3db36170-106e-49c8-9866-e25759bdd7f9">BCRYPT_DSA_KEY_BLOB</a> structure immediately followed by the key data.



#### BCRYPT_DSA_PUBLIC_BLOB

Export a DSA public key. The <i>pbOutput</i> buffer receives a <a href="https://msdn.microsoft.com/3db36170-106e-49c8-9866-e25759bdd7f9">BCRYPT_DSA_KEY_BLOB</a> structure immediately followed by the key data.



#### BCRYPT_ECCPRIVATE_BLOB

Export an <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">elliptic curve cryptography</a> (ECC) <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>. The <i>pbOutput</i> buffer receives a <a href="https://msdn.microsoft.com/e60f6630-e4b0-4f35-a3cf-95dbcb007124">BCRYPT_ECCKEY_BLOB</a> structure immediately followed by the key data.



#### BCRYPT_ECCPUBLIC_BLOB

Export an ECC public key. The <i>pbOutput</i> buffer receives a <a href="https://msdn.microsoft.com/e60f6630-e4b0-4f35-a3cf-95dbcb007124">BCRYPT_ECCKEY_BLOB</a> structure immediately followed by the key data.



#### BCRYPT_PUBLIC_KEY_BLOB

Export a generic public key of any type. The type of key in this BLOB is determined by the <b>Magic</b> member of the <a href="https://msdn.microsoft.com/ae7e8db3-858d-4573-afe1-c9bc14d76480">BCRYPT_KEY_BLOB</a> structure.



#### BCRYPT_PRIVATE_KEY_BLOB

Export a generic private key of any type.  The private key does not necessarily contain the public key. The type of key in this BLOB is determined by the <b>Magic</b> member of the <a href="https://msdn.microsoft.com/ae7e8db3-858d-4573-afe1-c9bc14d76480">BCRYPT_KEY_BLOB</a> structure.



#### BCRYPT_RSAFULLPRIVATE_BLOB

Export a full RSA public/private key pair. The <i>pbOutput</i> buffer receives a <a href="https://msdn.microsoft.com/bbf3f4b9-5c69-4212-bb23-34bb2c84185c">BCRYPT_RSAKEY_BLOB</a> structure immediately followed by the key data. This BLOB will include additional key material compared to the <b>BCRYPT_RSAPRIVATE_BLOB</b> type.



#### BCRYPT_RSAPRIVATE_BLOB

Export an RSA public/private key pair. The <i>pbOutput</i> buffer receives a <a href="https://msdn.microsoft.com/bbf3f4b9-5c69-4212-bb23-34bb2c84185c">BCRYPT_RSAKEY_BLOB</a> structure immediately followed by the key data.



#### BCRYPT_RSAPUBLIC_BLOB

Export an RSA public key. The <i>pbOutput</i> buffer receives a <a href="https://msdn.microsoft.com/bbf3f4b9-5c69-4212-bb23-34bb2c84185c">BCRYPT_RSAKEY_BLOB</a> structure immediately followed by the key data.



#### LEGACY_DH_PRIVATE_BLOB

Export a legacy <a href="https://msdn.microsoft.com/c759e6e1-f7af-4cd6-a67e-ff0da1e91eb1">Diffie-Hellman Version 3 Private Key BLOB</a> that contains a Diffie-Hellman public/private key pair that can be imported by using <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CryptoAPI</a>.



#### LEGACY_DH_PUBLIC_BLOB

Export a legacy <a href="https://msdn.microsoft.com/c759e6e1-f7af-4cd6-a67e-ff0da1e91eb1">Diffie-Hellman Version 3 Private Key BLOB</a> that contains a Diffie-Hellman public key that can be imported by using CryptoAPI.



#### LEGACY_DSA_PRIVATE_BLOB

Export a DSA public/private key pair in a form that can be imported by using CryptoAPI.



#### LEGACY_DSA_PUBLIC_BLOB

Export a DSA public key in a form that can be imported by using CryptoAPI.



#### LEGACY_RSAPRIVATE_BLOB

Export an RSA public/private key pair in a form that can be imported by using CryptoAPI.



#### LEGACY_RSAPUBLIC_BLOB

Export an RSA public key in a form that can be imported by using CryptoAPI.



#### NCRYPT_CIPHER_KEY_BLOB

Export a cipher key in a <a href="https://msdn.microsoft.com/387F05A3-C6E2-48EE-8FD0-C0A45E752300">NCRYPT_KEY_BLOB_HEADER</a> structure.

<b>Windows 8 and Windows Server 2012:  </b>Support for this value begins.



#### NCRYPT_OPAQUETRANSPORT_BLOB

Export a key in a format that is specific to a single CSP and is suitable for transport. Opaque BLOBs are not transferable and must be imported by using the same CSP that generated the BLOB.



#### NCRYPT_PKCS7_ENVELOPE_BLOB

Export a PKCS #7 envelope BLOB. The parameters identified by the <i>pParameterList</i> parameter either can or must contain the following parameters, as indicated by the Required or optional column.

<table>
<tr>
<th>Parameter</th>
<th>Required or optional</th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/474d3c0d-ae14-448a-a56d-25abc7e5de88">NCRYPTBUFFER_CERT_BLOB</a>


</td>
<td>
Required

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/474d3c0d-ae14-448a-a56d-25abc7e5de88">NCRYPTBUFFER_PKCS_ALG_OID</a>


</td>
<td>
Required

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/474d3c0d-ae14-448a-a56d-25abc7e5de88">NCRYPTBUFFER_PKCS_ALG_PARAM</a>


</td>
<td>
Optional

</td>
</tr>
</table>
 



#### NCRYPT_PKCS8_PRIVATE_KEY_BLOB

Export a PKCS #8 private key BLOB. The parameters identified by the <i>pParameterList</i> parameter either can or must contain the following parameters, as indicated by the Required or optional column.

<table>
<tr>
<th>Parameter</th>
<th>Required or optional</th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/474d3c0d-ae14-448a-a56d-25abc7e5de88">NCRYPTBUFFER_PKCS_ALG_OID</a>


</td>
<td>
Optional

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/474d3c0d-ae14-448a-a56d-25abc7e5de88">NCRYPTBUFFER_PKCS_ALG_PARAM</a>


</td>
<td>
Optional

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/474d3c0d-ae14-448a-a56d-25abc7e5de88">NCRYPTBUFFER_PKCS_SECRET</a>


</td>
<td>
Optional

</td>
</tr>
</table>
 



#### NCRYPT_PROTECTED_KEY_BLOB

Export a protected key in a <a href="https://msdn.microsoft.com/387F05A3-C6E2-48EE-8FD0-C0A45E752300">NCRYPT_KEY_BLOB_HEADER</a> structure.

<b>Windows 8 and Windows Server 2012:  </b>Support for this value begins.


### -param pParameterList [in, optional]

The address of an <a href="https://msdn.microsoft.com/ae4673ab-81cd-4604-bafa-8d8c66003aba">NCryptBufferDesc</a> structure that receives parameter information for the key. This parameter can be <b>NULL</b> if this information is not needed.


### -param pbOutput [out, optional]

The address of a buffer that receives the key BLOB. The <i>cbOutput</i> parameter contains the size of this buffer. If this parameter is <b>NULL</b>, this function will place the required size, in bytes, in the <b>DWORD</b> pointed to by the <i>pcbResult</i> parameter.


### -param cbOutput [in]

The size, in bytes, of the <i>pbOutput</i> buffer.


### -param pcbResult [out]

The address of a <b>DWORD</b> variable that receives the number of bytes copied to the <i>pbOutput</i> buffer. If the <i>pbOutput</i> parameter is <b>NULL</b>, this function will place the required size, in bytes, in the <b>DWORD</b> pointed to by this parameter.


### -param dwFlags [in]

Flags that modify function behavior. This can be zero or a combination of one or more of the following values.  The set of valid flags is specific to each key storage provider. The following flag applies to all providers.

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
<dt><b>NTE_BAD_KEY_STATE</b></dt>
</dl>
</td>
<td width="60%">
The key specified by the <i>hKey</i> parameter is not valid. The most common cause of this error is that the key was not completed by using the <a href="https://msdn.microsoft.com/4386030d-4ce6-4b2e-adc5-a15ddc869349">NCryptFinalizeKey</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The key specified by the <i>hKey</i> parameter cannot be exported into the BLOB type specified by the <i>pszBlobType</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hKey</i> or the <i>hExportKey</i> parameter is not valid.

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
</table>
 




## -remarks



A service must not call this function from its <a href="http://go.microsoft.com/fwlink/p/?linkid=137250">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.




## -see-also




<a href="https://msdn.microsoft.com/474d3c0d-ae14-448a-a56d-25abc7e5de88">NCryptBuffer</a>
 

 

