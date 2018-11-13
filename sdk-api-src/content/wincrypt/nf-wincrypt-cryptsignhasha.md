---
UID: NF:wincrypt.CryptSignHashA
title: CryptSignHashA function
author: windows-sdk-content
description: Signs data.
old-location: security\cryptsignhash.htm
tech.root: seccrypto
ms.assetid: 9cf0de04-fdad-457d-8137-16d98f915cd5
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CRYPT_NOHASHOID, CRYPT_TYPE2_FORMAT, CRYPT_X931_FORMAT, CryptSignHash, CryptSignHash function [Security], CryptSignHashA, CryptSignHashW, _crypto2_cryptsignhash, security.cryptsignhash, wincrypt/CryptSignHash, wincrypt/CryptSignHashA, wincrypt/CryptSignHashW
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
req.unicode-ansi: CryptSignHashW (Unicode) and CryptSignHashA (ANSI)
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
 - CryptSignHash
 - CryptSignHashA
 - CryptSignHashW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptSignHashA function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptSignHash</b> function signs data. Because all signature algorithms are asymmetric and thus slow, CryptoAPI does not allow data to be signed directly. Instead, data is first <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hashed</a>, and <b>CryptSignHash</b> is used to sign the hash.


## -parameters




### -param hHash [in]

Handle of the <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash object</a> to be signed.


### -param dwKeySpec [in]

Identifies the private key to use from the provider's container. It can be AT_KEYEXCHANGE or AT_SIGNATURE. 




The signature algorithm used is specified when the key pair is originally created.

The only signature algorithm that the Microsoft Base Cryptographic Provider supports is the RSA Public Key algorithm.


### -param szDescription [in]

This parameter is no longer used and must be set to <b>NULL</b> to prevent security vulnerabilities. However, it is still supported for backward compatibility in the Microsoft Base Cryptographic Provider.


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
Used with RSA providers. The hash <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) is not placed in the RSA public key encryption. If this flag is not set, the hash OID in the default signature is as specified in the definition of DigestInfo in PKCS #1. 



							

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
Use the RSA signature padding method specified in the ANSI X9.31 standard.

</td>
</tr>
</table>
 


### -param pbSignature [out]

A pointer to a buffer receiving the signature data. 




This parameter can be <b>NULL</b> to set the buffer size for memory allocation purposes. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pdwSigLen [in, out]

A pointer to a <b>DWORD</b> value that specifies the size, in bytes, of the <i>pbSignature</i> buffer. When the function returns, the <b>DWORD</b> value contains the number of bytes stored in the buffer. 




<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data fits in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns



If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call 
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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer specified by the <i>pbSignature</i> parameter is not large enough to hold the returned data. The required buffer size, in bytes, is in the <i>pdwSigLen</i><b>DWORD</b> value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_ALGID</b></dt>
</dl>
</td>
<td width="60%">
The <i>hHash</i> handle specifies an algorithm that this CSP does not support, or the <i>dwKeySpec</i> parameter has an incorrect value.

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
<dt><b>NTE_BAD_UID</b></dt>
</dl>
</td>
<td width="60%">
The CSP context that was specified when the hash object was created cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NO_KEY</b></dt>
</dl>
</td>
<td width="60%">
The private key specified by <i>dwKeySpec</i> does not exist.

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



Before calling this function, the 
<a href="https://msdn.microsoft.com/05e3db57-8d83-48e2-8590-68039ea27253">CryptCreateHash</a> function must be called to get a handle to a hash object. The 
<a href="https://msdn.microsoft.com/ec1482a2-c2cb-4c5f-af9c-d493134413d6">CryptHashData</a> or 
<a href="https://msdn.microsoft.com/75781993-7faf-4149-80cc-ae50dbd4de2a">CryptHashSessionKey</a> function is then used to add the data or session keys to the hash object. The <b>CryptSignHash</b> function completes the hash.

While the DSS CSP supports hashing with both the MD5 and the SHA hash algorithms, the DSS CSP only supports signing SHA hashes.

After this function is called, no more data can be added to the hash. Additional calls to <a href="https://msdn.microsoft.com/ec1482a2-c2cb-4c5f-af9c-d493134413d6">CryptHashData</a> or <a href="https://msdn.microsoft.com/75781993-7faf-4149-80cc-ae50dbd4de2a">CryptHashSessionKey</a> fail.

After the application finishes using the hash, 
destroy the hash object by calling the <a href="https://msdn.microsoft.com/0a4d6086-5c4c-4e1e-9ab9-b35ee49ffcae">CryptDestroyHash</a> function.

By default, the Microsoft RSA providers use the PKCS #1 padding method for the signature. The hash OID in the <b>DigestInfo</b> element of the signature is automatically set to the algorithm OID associated with the hash object. Using the <b>CRYPT_NOHASHOID</b> flag will cause this OID to be omitted from the signature.

Occasionally, a hash value that has been generated elsewhere must be signed. This can be done by using the following sequence of operations:

<ol>
<li>Create a hash object by using 
<a href="https://msdn.microsoft.com/05e3db57-8d83-48e2-8590-68039ea27253">CryptCreateHash</a>.</li>
<li>Set the hash value in the hash object by using the <b>HP_HASHVAL</b> value of the <i>dwParam</i> parameter in <a href="https://msdn.microsoft.com/0c8d3ef9-e7b5-4e49-a2f8-9c85b16549da">CryptSetHashParam</a>.</li>
<li>Sign the hash value by using 
<b>CryptSignHash</b> and obtain a digital signature block.</li>
<li>Destroy the hash object by using 
<a href="https://msdn.microsoft.com/0a4d6086-5c4c-4e1e-9ab9-b35ee49ffcae">CryptDestroyHash</a>.</li>
</ol>

#### Examples

The following example shows signing data by first hashing the data to be signed and then signing the hash by using the <b>CryptSignHash</b> function.


```cpp
//-------------------------------------------------------------
// Declare and initialize variables.

HCRYPTPROV hProv;
BYTE *pbBuffer= (BYTE *)"Sample data that is to be signed.";
DWORD dwBufferLen = strlen((char *)pbBuffer)+1;
HCRYPTHASH hHash;

//--------------------------------------------------------------------
// This code assumes that a cryptographic context handle, hProv,
// and a hash handle, hHash, are available.
// For code needed to acquire the context, see "Example C Program: 
// Signing a Hash and Verifying the Hash Signature."

//--------------------------------------------------------------------
// Compute the cryptographic hash of the buffer.

if(CryptHashData(
   hHash, 
   pbBuffer, 
   dwBufferLen, 
   0)) 
{
     printf("The data buffer has been hashed.\n");
}
else
{
     printf("Error during CryptHashData.\n");
     exit(1);
}
//--------------------------------------------------------------------
// Determine the size of the signature and allocate memory.

dwSigLen= 0;
if(CryptSignHash(
   hHash, 
   AT_SIGNATURE, 
   szDescription, 
   0, 
   NULL, 
   &dwSigLen)) 
{
     printf("Signature length %d found.\n",dwSigLen);
}
else
{
     printf("Error during CryptSignHash\n");
     exit(1);
}
//--------------------------------------------------------------------
// Allocate memory for the signature buffer.

if(pbSignature = (BYTE *)malloc(dwSigLen))
{
     printf("Memory allocated for the signature.\n");
}
else
{
     printf("Out of memory\n");
     exit(1);
}
//--------------------------------------------------------------------
// Sign the hash object.

if(CryptSignHash(
   hHash, 
   AT_SIGNATURE, 
   szDescription, 
   0, 
   pbSignature, 
   &dwSigLen)) 
{
     printf("pbSignature is the hash signature.\n");
}
else
{
     printf("Error during CryptSignHash.\n");
     exit(1);
}
//--------------------------------------------------------------------
// Destroy the hash object.

if(hHash) 
  CryptDestroyHash(hHash);
```


For a complete example including the  context for this code, see 
<a href="https://msdn.microsoft.com/72f5d30a-efd5-4bf5-8057-cb73e5aa0514">Example C Program: Signing a Hash and Verifying the Hash Signature</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/05e3db57-8d83-48e2-8590-68039ea27253">CryptCreateHash</a>



<a href="https://msdn.microsoft.com/0a4d6086-5c4c-4e1e-9ab9-b35ee49ffcae">CryptDestroyHash</a>



<a href="https://msdn.microsoft.com/ec1482a2-c2cb-4c5f-af9c-d493134413d6">CryptHashData</a>



<a href="https://msdn.microsoft.com/75781993-7faf-4149-80cc-ae50dbd4de2a">CryptHashSessionKey</a>



<a href="https://msdn.microsoft.com/3119eabc-90ff-42c6-b3fa-e8be625f6d1e">CryptVerifySignature</a>



<a href="cryptography_functions.htm">Hash and Digital Signature Functions</a>
 

 

