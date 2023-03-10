---
UID: NF:ncrypt.NCryptDeriveKey
title: NCryptDeriveKey function (ncrypt.h)
description: Derives a key from a secret agreement value. (NCryptDeriveKey)
helpviewer_keywords: ["BCRYPT_KDF_HASH","BCRYPT_KDF_HMAC","BCRYPT_KDF_SP80056A_CONCAT","BCRYPT_KDF_TLS_PRF","KDF_USE_SECRET_AS_HMAC_KEY_FLAG","NCryptDeriveKey","NCryptDeriveKey function [Security]","ncrypt/NCryptDeriveKey","security.ncryptderivekey"]
old-location: security\ncryptderivekey.htm
tech.root: security
ms.assetid: 0ff08c6a-5f30-43ca-9db8-cda3e0704b0a
ms.date: 12/05/2018
ms.keywords: BCRYPT_KDF_HASH, BCRYPT_KDF_HMAC, BCRYPT_KDF_SP80056A_CONCAT, BCRYPT_KDF_TLS_PRF, KDF_USE_SECRET_AS_HMAC_KEY_FLAG, NCryptDeriveKey, NCryptDeriveKey function [Security], ncrypt/NCryptDeriveKey, security.ncryptderivekey
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NCryptDeriveKey
 - ncrypt/NCryptDeriveKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ncrypt.dll
api_name:
 - NCryptDeriveKey
---

# NCryptDeriveKey function


## -description

The <b>NCryptDeriveKey</b> function derives a key from a secret agreement value. This function is intended to be used as part of a secret agreement procedure using persisted secret agreement keys. To derive key material by using a  persisted secret instead, use the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptkeyderivation">NCryptKeyDerivation</a> function.

## -parameters

### -param hSharedSecret [in]

The secret agreement handle to create the key from. This handle is obtained from the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptsecretagreement">NCryptSecretAgreement</a> function.

### -param pwszKDF [in]

A pointer to a null-terminated Unicode string that identifies the <i>key derivation function</i> (KDF) to use to derive the key. This can be one of the following strings.



#### BCRYPT_KDF_HASH (L"HASH")

Use the hash key derivation function. 

If the <i>cbDerivedKey</i> parameter is less than the size of the derived key, this function will only copy the specified number of bytes to the <i>pbDerivedKey</i> buffer. If the <i>cbDerivedKey</i> parameter is greater than the size of the derived key, this function will copy the key to the <i>pbDerivedKey</i> buffer and set the variable pointed to by the <i>pcbResult</i> to the actual number of bytes copied.

The parameters identified by the <i>pParameterList</i> parameter either can or must contain the following parameters, as indicated by the Required or optional column.

<table>
<tr>
<th>Parameter</th>
<th>Description</th>
<th>Required or optional</th>
</tr>
<tr>
<td>
<b>KDF_HASH_ALGORITHM</b>

</td>
<td>
A null-terminated Unicode string that identifies the hash algorithm to use. This can be one of the standard hash algorithm identifiers from <a href="/windows/desktop/SecCNG/cng-algorithm-identifiers">CNG Algorithm Identifiers</a> or the identifier for another registered hash algorithm.

If this parameter is not specified, the SHA1 hash algorithm is used.

</td>
<td>
Optional

</td>
</tr>
<tr>
<td>
<b>KDF_SECRET_PREPEND</b>

</td>
<td>
A value to add to the beginning of the message input to the hash function. For more information, see Remarks.

</td>
<td>
Optional

</td>
</tr>
<tr>
<td>
<b>KDF_SECRET_APPEND</b>

</td>
<td>
A value to add to the end of the message input to the hash function. For more information, see Remarks.

</td>
<td>
Optional

</td>
</tr>
</table>
 

The call to the KDF is made as shown in the following pseudocode.


``` syntax
KDF-Prepend = KDF_SECRET_PREPEND[0] + 
    KDF_SECRET_PREPEND[1] + 
    ... +
    KDF_SECRET_PREPEND[n]

KDF-Append = KDF_SECRET_APPEND[0] + 
    KDF_SECRET_APPEND[1] + 
    ... + 
    KDF_SECRET_APPEND[n]

KDF-Output = Hash(
    KDF-Prepend + 
    hSharedSecret + 
    KDF-Append)
```



#### BCRYPT_KDF_HMAC (L"HMAC")

Use the <a href="/windows/desktop/SecGloss/h-gly">Hash-Based Message Authentication Code</a> (HMAC) key derivation function. 

If the <i>cbDerivedKey</i> parameter is less than the size of the derived key, this function will only copy the specified number of bytes to the <i>pbDerivedKey</i> buffer. If the <i>cbDerivedKey</i> parameter is greater than the size of the derived key, this function will copy the key to the <i>pbDerivedKey</i> buffer and set the variable pointed to by the <i>pcbResult</i> to the actual number of bytes copied.

The parameters identified by the <i>pParameterList</i> parameter either can or must contain the following parameters, as indicated by the Required or optional column.

<table>
<tr>
<th>Parameter</th>
<th>Description</th>
<th>Required or optional</th>
</tr>
<tr>
<td>
<b>KDF_HASH_ALGORITHM</b>

</td>
<td>
A null-terminated Unicode string that identifies the hash algorithm to use. This can be one of the standard hash algorithm identifiers from <a href="/windows/desktop/SecCNG/cng-algorithm-identifiers">CNG Algorithm Identifiers</a> or the identifier for another registered hash algorithm.

If this parameter is not specified, the SHA1 hash algorithm is used.

</td>
<td>
Optional

</td>
</tr>
<tr>
<td>
<b>KDF_HMAC_KEY</b>

</td>
<td>
The key to use for the <a href="/windows/desktop/SecGloss/p-gly">pseudo-random function</a> (PRF).

</td>
<td>
Optional

</td>
</tr>
<tr>
<td>
<b>KDF_SECRET_PREPEND</b>

</td>
<td>
A value to add to the beginning of the message input to the hash function. For more information, see Remarks.

</td>
<td>
Optional

</td>
</tr>
<tr>
<td>
<b>KDF_SECRET_APPEND</b>

</td>
<td>
A value to add to the end of the message input to the hash function. For more information, see Remarks.

</td>
<td>
Optional

</td>
</tr>
</table>
 

The call to the KDF is made as shown in the following pseudocode.


``` syntax
KDF-Prepend = KDF_SECRET_PREPEND[0] + 
    KDF_SECRET_PREPEND[1] + 
    ... +
    KDF_SECRET_PREPEND[n]

KDF-Append = KDF_SECRET_APPEND[0] + 
    KDF_SECRET_APPEND[1] + 
    ... + 
    KDF_SECRET_APPEND[n]

KDF-Output = HMAC-Hash(
    KDF_HMAC_KEY,
    KDF-Prepend + 
    hSharedSecret + 
    KDF-Append)
```



#### BCRYPT_KDF_TLS_PRF (L"TLS_PRF")

Use the <a href="/windows/desktop/SecGloss/t-gly">transport layer security</a> (TLS) <a href="/windows/desktop/SecGloss/p-gly">pseudo-random function</a> (PRF) key derivation function. The size of the derived key is always 48 bytes, so the <i>cbDerivedKey</i> parameter must be 48.

The parameters identified by the <i>pParameterList</i> parameter either can or must contain the following parameters, as indicated by the Required or optional column.

<table>
<tr>
<th>Parameter</th>
<th>Description</th>
<th>Required or optional</th>
</tr>
<tr>
<td>
<b>KDF_TLS_PRF_LABEL</b>

</td>
<td>
An ANSI string that contains the PRF label.

</td>
<td>
Required

</td>
</tr>
<tr>
<td>
<b>KDF_TLS_PRF_SEED</b>

</td>
<td>
The PRF seed. The seed must be 64 bytes long.

</td>
<td>
Required

</td>
</tr>
</table>
 

The call to the KDF is made as shown in the following pseudocode.


``` syntax
KDF-Output = PRF(
    hSharedSecret, 
    KDF_TLS_PRF_LABEL, 
    KDF_TLS_PRF_SEED)
```



#### BCRYPT_KDF_SP80056A_CONCAT (L"SP800_56A_CONCAT")

Use the SP800-56A key derivation function.

The parameters identified by the <i>pParameterList</i> parameter either can or must contain the following parameters, as indicated by the Required or optional column. All parameter values are treated as opaque byte arrays.


<table>
<tr>
<th>Parameter</th>
<th>Description</th>
<th>Required or optional</th>
</tr>
<tr>
<td>
<b>KDF_ALGORITHMID</b>

</td>
<td>
Specifies the <b>AlgorithmID</b> subfield of the <b>OtherInfo</b> field in the SP800-56A key derivation function. Indicates the intended purpose of the derived key.

</td>
<td>
Required

</td>
</tr>
<tr>
<td>
<b>KDF_PARTYUINFO</b>

</td>
<td>
Specifies the <b>PartyUInfo</b> subfield of the <b>OtherInfo</b> field in the SP800-56A key derivation function. The field contains public information contributed by the initiator.

</td>
<td>
Required

</td>
</tr>
<tr>
<td>
<b>KDF_PARTYVINFO</b>

</td>
<td>
Specifies the <b>PartyVInfo</b> subfield of the <b>OtherInfo</b> field in the SP800-56A key derivation function. The field contains public information contributed by the responder.

</td>
<td>
Required

</td>
</tr>
<tr>
<td>
<b>KDF_SUPPPUBINFO</b>

</td>
<td>
Specifies the <b>SuppPubInfo</b> subfield of the <b>OtherInfo</b> field in the SP800-56A key derivation function. The field contains public information known to both initiator and responder.

</td>
<td>
Optional

</td>
</tr>
<tr>
<td>
<b>KDF_SUPPPRIVINFO</b>

</td>
<td>
Specifies the <b>SuppPrivInfo</b> subfield of the <b>OtherInfo</b> field in the SP800-56A key derivation function.  It contains private information known to both initiator and responder, such as a shared secret.

</td>
<td>
Optional

</td>
</tr>
</table>
 

The call to the KDF is made as shown in the following pseudocode.


``` syntax
KDF-Output = SP_800-56A_KDF(
	   hSharedSecret,
	   KDF_ALGORITHMID,
	   KDF_PARTYUINFO,
	   KDF_PARTYVINFO,
	   KDF_SUPPPUBINFO,
	   KDF_SUPPPRIVINFO)
```

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.



####

### -param pParameterList [in, optional]

The address of a <a href="/windows/win32/api/bcrypt/ns-bcrypt-bcryptbufferdesc">NCryptBufferDesc</a> structure that contains the KDF parameters. This parameter is optional and can be <b>NULL</b> if it is not needed.

### -param pbDerivedKey [out, optional]

The address of a buffer that receives the key. The <i>cbDerivedKey</i> parameter contains the size of this buffer. If this parameter is <b>NULL</b>, this function will place the required size, in bytes, in the <b>DWORD</b> pointed to by the <i>pcbResult</i> parameter.

### -param cbDerivedKey [in]

The size, in bytes, of the <i>pbDerivedKey</i> buffer.

### -param pcbResult [out]

A pointer to a <b>DWORD</b> that receives the number of bytes that were copied to the <i>pbDerivedKey</i> buffer. If the <i>pbDerivedKey</i> parameter is <b>NULL</b>, this function will place the required size, in bytes, in the <b>DWORD</b> pointed to by this parameter.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. This can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KDF_USE_SECRET_AS_HMAC_KEY_FLAG"></a><a id="kdf_use_secret_as_hmac_key_flag"></a><dl>
<dt><b>KDF_USE_SECRET_AS_HMAC_KEY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The secret agreement value will also serve as the HMAC key. If this flag is specified, the <b>KDF_HMAC_KEY</b> parameter should not be included in the set of parameters in the <i>pParameterList</i> parameter. This flag is only used by the <b>BCRYPT_KDF_HMAC</b> key derivation function.

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
<dt><b>NTE_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hSharedSecret</i> parameter is not valid.

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

The <a href="/previous-versions/windows/desktop/legacy/aa375370(v=vs.85)">BCryptBufferDesc</a> structure in the <i>pParameterList</i> parameter can contain more than one of the <b>KDF_SECRET_PREPEND</b> and <b>KDF_SECRET_APPEND</b> parameters. If more than one of these parameters is specified, the parameter values are concatenated in the order in which they are contained in the array before the KDF is called. For example, assume the following parameter values are specified.


```cpp
BYTE pbValue0[1] = {0x01};
BYTE pbValue1[2] = {0x04, 0x05};
BYTE pbValue2[3] = {0x10, 0x11, 0x12};
BYTE pbValue3[4] = {0x20, 0x21, 0x22, 0x23};

Parameter[0].type = KDF_SECRET_APPEND
Parameter[0].value = pbValue0;
Parameter[0].length = sizeof  (pbValue0);
Parameter[1].type = KDF_SECRET_PREPEND
Parameter[1].value = pbValue1;
Parameter[1].length = sizeof (pbValue1);
Parameter[2].type = KDF_SECRET_APPEND
Parameter[2].value = pbValue2;
Parameter[2].length = sizeof (pbValue2);
Parameter[3].type = KDF_SECRET_PREPEND
Parameter[3].value = pbValue3;
Parameter[3].length = sizeof (pbValue3);

```


If the above parameter values are specified, the concatenated values to the actual KDF are as follows.


``` syntax
Type: KDF_SECRET_PREPEND
Value: {0x04, 0x05, 0x20, 0x21, 0x22, 0x23}, length 6

Type: KDF_SECRET_APPEND
Value: {0x01, 0x10, 0x11, 0x12}, length 4

```

A service must not call this function from its <a href="/windows/win32/api/winsvc/nf-winsvc-startservicea">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.

## -see-also

<a href="/windows/win32/api/bcrypt/ns-bcrypt-bcryptbufferdesc">NCryptBufferDesc</a>
