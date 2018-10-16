---
UID: NF:wincrypt.CryptVerifySignatureW
title: CryptVerifySignatureW function
author: windows-sdk-content
description: Verifies the signature of a hash object.
old-location: security\cryptverifysignature.htm
tech.root: seccrypto
ms.assetid: 3119eabc-90ff-42c6-b3fa-e8be625f6d1e
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: CRYPT_NOHASHOID, CRYPT_TYPE2_FORMAT, CRYPT_X931_FORMAT, CryptVerifySignature, CryptVerifySignature function [Security], CryptVerifySignatureA, CryptVerifySignatureW, _crypto2_cryptverifysignature, security.cryptverifysignature, wincrypt/CryptVerifySignature, wincrypt/CryptVerifySignatureA, wincrypt/CryptVerifySignatureW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CryptVerifySignatureW (Unicode) and CryptVerifySignatureA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Security-cryptoapi-l1-1-0.dll
 - cryptsp.dll
api_name:
 - CryptVerifySignature
 - CryptVerifySignatureA
 - CryptVerifySignatureW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptVerifySignatureW function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptVerifySignature</b> function verifies the signature of a <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash object</a>.

Before calling this function, 
<a href="https://msdn.microsoft.com/05e3db57-8d83-48e2-8590-68039ea27253">CryptCreateHash</a> must be called to create the handle of a hash object. 
<a href="https://msdn.microsoft.com/ec1482a2-c2cb-4c5f-af9c-d493134413d6">CryptHashData</a> or 
<a href="https://msdn.microsoft.com/75781993-7faf-4149-80cc-ae50dbd4de2a">CryptHashSessionKey</a> is then used to add data or <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">session keys</a> to the hash object.

After <b>CryptVerifySignature</b> completes, only 
<a href="https://msdn.microsoft.com/0a4d6086-5c4c-4e1e-9ab9-b35ee49ffcae">CryptDestroyHash</a> can be called by using the <i>hHash</i> handle.


## -parameters




### -param hHash [in]

A handle to the hash object to verify.


### -param pbSignature [in]

The address of the signature data to be verified.


### -param dwSigLen [in]

The number of bytes in the <i>pbSignature</i> signature data.


### -param hPubKey [in]

A handle to the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> to use to authenticate the signature. This public key must belong to the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key pair</a> that was originally used to create the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">digital signature</a>.


### -param szDescription [in]

This parameter should no longer be used and must be set to <b>NULL</b> to prevent security vulnerabilities. However, it is still supported for backward compatibility in the Microsoft Base Cryptographic Provider.


### -param dwFlags [in]

The following flag values are defined. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_NOHASHOID"></a><a id="crypt_nohashoid"></a><dl>
<dt><b>CRYPT_NOHASHOID</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
This flag is used with RSA providers. When verifying the signature, the hash <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) is not expected to be present or checked. If this flag is not set, the hash OID in the default signature is verified as specified in the definition of DigestInfo in PKCS #7. 



							

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_TYPE2_FORMAT"></a><a id="crypt_type2_format"></a><dl>
<dt><b>CRYPT_TYPE2_FORMAT</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
This flag is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_X931_FORMAT"></a><a id="crypt_x931_format"></a><dl>
<dt><b>CRYPT_X931_FORMAT</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Use X.931 support for the FIPS 186-2–compliant version of RSA (rDSA).

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The error codes prefaced by "NTE" are generated by the particular CSP you are using. Some possible error codes follow.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters specifies a handle that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters contains a value that is not valid. This is most often a pointer that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter is nonzero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_HASH</b></dt>
</dl>
</td>
<td width="60%">
The hash object specified by the <i>hHash</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_KEY</b></dt>
</dl>
</td>
<td width="60%">
The <i>hPubKey</i> parameter does not contain a handle to a valid <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
The signature was not valid. This might be because the data itself has changed, the description string did not match, or the wrong public key was specified by <i>hPubKey</i>.

This error can also be returned if the hashing or signature algorithms do not match the ones used to create the signature.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_UID</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) context that was specified when the hash object was created cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The CSP ran out of memory during the operation.

</td>
</tr>
</table>
 




## -remarks



The <b>CryptVerifySignature</b> function completes the hash. After this call, no more data can be added to the hash. Additional calls to 
<a href="https://msdn.microsoft.com/ec1482a2-c2cb-4c5f-af9c-d493134413d6">CryptHashData</a> or 
<a href="https://msdn.microsoft.com/75781993-7faf-4149-80cc-ae50dbd4de2a">CryptHashSessionKey</a> fail. After the application is done with the hash, 
<a href="https://msdn.microsoft.com/0a4d6086-5c4c-4e1e-9ab9-b35ee49ffcae">CryptDestroyHash</a> should be called to destroy the hash object.

If you generate a signature by using the .NET Framework APIs and try to verify it by using the <b>CryptVerifySignature</b> function, the function will fail and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will return  <b>NTE_BAD_SIGNATURE</b>. This is due to the different byte orders between the native Win32 API  and the .NET Framework API.

The native cryptography API uses little-endian byte order while the .NET Framework API uses big-endian byte order. If you are verifying a  signature generated by using a .NET Framework API, you must swap the order of signature bytes before calling the <b>CryptVerifySignature</b> function to verify the signature.


#### Examples

For an example that uses the <b>CryptVerifySignature</b> function, see <a href="https://msdn.microsoft.com/72f5d30a-efd5-4bf5-8057-cb73e5aa0514">Example C Program: Signing a Hash and Verifying the Hash Signature</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/05e3db57-8d83-48e2-8590-68039ea27253">CryptCreateHash</a>



<a href="https://msdn.microsoft.com/0a4d6086-5c4c-4e1e-9ab9-b35ee49ffcae">CryptDestroyHash</a>



<a href="https://msdn.microsoft.com/ec1482a2-c2cb-4c5f-af9c-d493134413d6">CryptHashData</a>



<a href="https://msdn.microsoft.com/75781993-7faf-4149-80cc-ae50dbd4de2a">CryptHashSessionKey</a>



<a href="https://msdn.microsoft.com/9cf0de04-fdad-457d-8137-16d98f915cd5">CryptSignHash</a>



<a href="cryptography_functions.htm">Hash and Digital Signature Functions</a>
 

 

