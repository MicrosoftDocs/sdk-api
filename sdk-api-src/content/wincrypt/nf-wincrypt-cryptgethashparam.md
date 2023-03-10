---
UID: NF:wincrypt.CryptGetHashParam
title: CryptGetHashParam function (wincrypt.h)
description: Retrieves data that governs the operations of a hash object.
helpviewer_keywords: ["CryptGetHashParam","CryptGetHashParam function [Security]","HP_ALGID","HP_HASHSIZE","HP_HASHVAL","_crypto2_cryptgethashparam","security.cryptgethashparam","wincrypt/CryptGetHashParam"]
old-location: security\cryptgethashparam.htm
tech.root: security
ms.assetid: ed008c07-1a40-4075-bdaa-eb7f7e12d9c3
ms.date: 12/05/2018
ms.keywords: CryptGetHashParam, CryptGetHashParam function [Security], HP_ALGID, HP_HASHSIZE, HP_HASHVAL, _crypto2_cryptgethashparam, security.cryptgethashparam, wincrypt/CryptGetHashParam
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptGetHashParam
 - wincrypt/CryptGetHashParam
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
 - CryptGetHashParam
---

# CryptGetHashParam function


## -description

<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptGetHashParam</b> function retrieves data that governs the operations of a hash object. The actual hash value can be retrieved by using this function.

## -parameters

### -param hHash [in]

Handle of the hash object to be queried.

### -param dwParam [in]

Query type. This parameter can be set to one of the following queries. 
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HP_ALGID"></a><a id="hp_algid"></a><dl>
<dt><b>HP_ALGID</b></dt>
<dt>Hash algorithm</dt>
</dl>
</td>
<td width="60%">
An 
<a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a> that indicates the algorithm specified when the hash object was created. For a list of hash algorithms, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="HP_HASHSIZE"></a><a id="hp_hashsize"></a><dl>
<dt><b>HP_HASHSIZE</b></dt>
<dt>Hash value size</dt>
</dl>
</td>
<td width="60%">
<b>DWORD</b> value indicating the number of bytes in the hash value. This value will vary depending on the hash algorithm. Applications must retrieve this value just before the HP_HASHVAL value so the correct amount of memory can be allocated.

</td>
</tr>
<tr>
<td width="40%"><a id="HP_HASHVAL"></a><a id="hp_hashval"></a><dl>
<dt><b>HP_HASHVAL</b></dt>
<dt>Hash value</dt>
</dl>
</td>
<td width="60%">
The hash value or message hash for the hash object specified by <i>hHash</i>. This value is generated based on the data supplied to the hash object earlier through the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashdata">CryptHashData</a> and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashsessionkey">CryptHashSessionKey</a> functions.

The <b>CryptGetHashParam</b> function completes the hash. After <b>CryptGetHashParam</b> has been called, no more data can be added to the hash. Additional calls to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashdata">CryptHashData</a> or <a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashsessionkey">CryptHashSessionKey</a> fail. After the application is done with the hash, 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdestroyhash">CryptDestroyHash</a> should be called to destroy the hash object.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  CSPs can add more values that this function can query.</div>
<div> </div>

### -param pbData [out]

A pointer to a buffer that receives the specified value data. The form of this data varies, depending on the value number. 


This parameter can be <b>NULL</b> to determine the memory size required.

### -param pdwDataLen [in, out]

A pointer to a <b>DWORD</b> value specifying the size, in bytes, of the <i>pbData</i> buffer. When the function returns, the <b>DWORD</b> value contains the number of bytes stored in the buffer. 


If <i>pbData</i> is <b>NULL</b>, set the value of <i>pdwDataLen</i> to zero.

<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data fits in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

### -param dwFlags [in]

Reserved for future use and must be zero.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. For extended error information, call 
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
If the buffer specified by the <i>pbData</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code and stores the required buffer size, in bytes, in the variable pointed to by <i>pdwDataLen</i>.

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
<dt><b>NTE_BAD_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwParam</i> parameter specifies an unknown value number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_UID</b></dt>
</dl>
</td>
<td width="60%">
The CSP context that was specified when the hash was created cannot be found.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdestroyhash">CryptDestroyHash</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetkeyparam">CryptGetKeyParam</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashdata">CryptHashData</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashsessionkey">CryptHashSessionKey</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsethashparam">CryptSetHashParam</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Hash and Digital Signature Functions</a>