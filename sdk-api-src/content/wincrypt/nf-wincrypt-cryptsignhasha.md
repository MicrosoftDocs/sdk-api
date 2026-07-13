---
UID: NF:wincrypt.CryptSignHashA
title: CryptSignHashA function (wincrypt.h)
description: Signs data. (CryptSignHashA)
helpviewer_keywords: ["CRYPT_NOHASHOID", "CRYPT_TYPE2_FORMAT", "CRYPT_X931_FORMAT", "CryptSignHashA", "wincrypt/CryptSignHashA"]
old-location: security\cryptsignhash.htm
tech.root: security
ms.assetid: 9cf0de04-fdad-457d-8137-16d98f915cd5
ms.date: 12/05/2018
ms.keywords: CRYPT_NOHASHOID, CRYPT_TYPE2_FORMAT, CRYPT_X931_FORMAT, CryptSignHash, CryptSignHash function [Security], CryptSignHashA, CryptSignHashW, _crypto2_cryptsignhash, security.cryptsignhash, wincrypt/CryptSignHash, wincrypt/CryptSignHashA, wincrypt/CryptSignHashW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptSignHashA
 - wincrypt/CryptSignHashA
dev_langs:
 - c++
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
---

# CryptSignHashA function


## -description

<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptSignHash</b> function signs data. Because all signature algorithms are asymmetric and thus slow, CryptoAPI does not allow data to be signed directly. Instead, data is first <a href="/windows/desktop/SecGloss/h-gly">hashed</a>, and <b>CryptSignHash</b> is used to sign the hash.

## -parameters

### -param hHash [in]

Handle of the <a href="/windows/desktop/SecGloss/h-gly">hash object</a> to be signed.

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
Used with RSA providers. The hash <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) is not placed in the RSA public key encryption. If this flag is not set, the hash OID in the default signature is as specified in the definition of DigestInfo in PKCS #1. 



							

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
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pdwSigLen [in, out]

A pointer to a <b>DWORD</b> value that specifies the size, in bytes, of the <i>pbSignature</i> buffer. When the function returns, the <b>DWORD</b> value contains the number of bytes stored in the buffer. 




<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data fits in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns

If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

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
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a> function must be called to get a handle to a hash object. The 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashdata">CryptHashData</a> or 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashsessionkey">CryptHashSessionKey</a> function is then used to add the data or session keys to the hash object. The <b>CryptSignHash</b> function completes the hash.

While the DSS CSP supports hashing with both the MD5 and the SHA hash algorithms, the DSS CSP only supports signing SHA hashes.

After this function is called, no more data can be added to the hash. Additional calls to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashdata">CryptHashData</a> or <a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashsessionkey">CryptHashSessionKey</a> fail.

After the application finishes using the hash, 
destroy the hash object by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdestroyhash">CryptDestroyHash</a> function.

By default, the Microsoft RSA providers use the PKCS #1 padding method for the signature. The hash OID in the <b>DigestInfo</b> element of the signature is automatically set to the algorithm OID associated with the hash object. Using the <b>CRYPT_NOHASHOID</b> flag will cause this OID to be omitted from the signature.

Occasionally, a hash value that has been generated elsewhere must be signed. This can be done by using the following sequence of operations:

<ol>
<li>Create a hash object by using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>.</li>
<li>Set the hash value in the hash object by using the <b>HP_HASHVAL</b> value of the <i>dwParam</i> parameter in <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsethashparam">CryptSetHashParam</a>.</li>
<li>Sign the hash value by using 
<b>CryptSignHash</b> and obtain a digital signature block.</li>
<li>Destroy the hash object by using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdestroyhash">CryptDestroyHash</a>.</li>
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
<a href="/windows/desktop/SecCrypto/example-c-program-signing-a-hash-and-verifying-the-hash-signature">Example C Program: Signing a Hash and Verifying the Hash Signature</a>.

<div class="code"></div>




> [!NOTE]
> The wincrypt.h header defines CryptSignHash as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdestroyhash">CryptDestroyHash</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashdata">CryptHashData</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashsessionkey">CryptHashSessionKey</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifysignaturea">CryptVerifySignature</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Hash and Digital Signature Functions</a>
