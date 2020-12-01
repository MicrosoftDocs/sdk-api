---
UID: NF:bcrypt.BCryptKeyDerivation
title: BCryptKeyDerivation function (bcrypt.h)
description: Derives a key without requiring a secret agreement.
helpviewer_keywords: ["BCryptKeyDerivation","BCryptKeyDerivation function [Security]","bcrypt/BCryptKeyDerivation","security.bcryptkeyderivation"]
old-location: security\bcryptkeyderivation.htm
tech.root: security
ms.assetid: D0B91FFE-2E72-4AE3-A84F-DC598C02CF53
ms.date: 12/05/2018
ms.keywords: BCryptKeyDerivation, BCryptKeyDerivation function [Security], bcrypt/BCryptKeyDerivation, security.bcryptkeyderivation
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BCryptKeyDerivation
 - bcrypt/BCryptKeyDerivation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
 - Ksecdd.sys
api_name:
 - BCryptKeyDerivation
---

# BCryptKeyDerivation function


## -description

The <b>BCryptKeyDerivation</b>  function derives a key without requiring a secret agreement. It is similar in functionality to <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptderivekey">BCryptDeriveKey</a> but does not require a BCRYPT_SECRET_HANDLE value as input.

## -parameters

### -param hKey [in]

Handle of the input key.

### -param pParameterList [in, optional]

Pointer to a  <b>BCryptBufferDesc</b> structure that contains the KDF parameters. This parameter is optional and can be <b>NULL</b> if it is not needed. 
The parameters can be specific to a key derivation function (KDF) or generic. The following table shows the required and optional parameters for specific KDFs implemented by the Microsoft Primitive provider.

<table>
<tr>
<th>KDF</th>
<th>Parameter</th>
<th>Required</th>
</tr>
<tr>
<td>SP800-108 HMAC in counter mode</td>
<td>KDF_LABEL</td>
<td>yes</td>
</tr>
<tr>
<td></td>
<td>KDF_CONTEXT</td>
<td>yes</td>
</tr>
<tr>
<td></td>
<td>KDF_HASH_ALGORITHM</td>
<td>yes</td>
</tr>
<tr>
<td>SP800-56A</td>
<td>KDF_ALGORITHMID</td>
<td>yes</td>
</tr>
<tr>
<td></td>
<td>KDF_PARTYUINFO</td>
<td>yes</td>
</tr>
<tr>
<td></td>
<td>KDF_PARTYVINFO</td>
<td>yes</td>
</tr>
<tr>
<td></td>
<td>KDF_HASH_ALGORITHM</td>
<td>yes</td>
</tr>
<tr>
<td></td>
<td>KDF_SUPPPUBINFO</td>
<td>no</td>
</tr>
<tr>
<td></td>
<td>KDF_SUPPPRIVINFO</td>
<td>no</td>
</tr>
<tr>
<td>PBKDF2</td>
<td>KDF_HASH_ALGORITHM</td>
<td>yes</td>
</tr>
<tr>
<td></td>
<td>KDF_SALT</td>
<td>yes</td>
</tr>
<tr>
<td></td>
<td>KDF_ITERATION_COUNT</td>
<td>no</td>
</tr>
<tr>
<td>CAPI_KDF</td>
<td>KDF_HASH_ALGORITHM</td>
<td>yes</td>
</tr>
</table>
 

The following generic parameter can be used:<ul>
<li>KDF_GENERIC_PARAMETER</li>
</ul>Generic parameters map to KDF specific parameters in the following manner:

SP800-108 HMAC in counter mode:<ul>
<li>KDF_GENERIC_PARAMETER = KDF_LABEL||0x00||KDF_CONTEXT</li>
</ul>


SP800-56A<ul>
<li>KDF_GENERIC_PARAMETER = KDF_ALGORITHMID || KDF_PARTYUINFO || KDF_PARTYVINFO {|| KDF_SUPPPUBINFO } {|| KDF_SUPPPRIVINFO }</li>
</ul>


PBKDF2<ul>
<li>KDF_GENERIC_PARAMETER = KDF_SALT </li>
<li>KDF_ITERATION_COUNT – defaults to 10000</li>
</ul>


CAPI_KDF<ul>
<li>KDF_GENERIC_PARAMETER = Not Used </li>
</ul>

### -param pbDerivedKey [out]

Address of a buffer that receives the key. The <i>cbDerivedKey</i> parameter contains the size of this buffer.

### -param cbDerivedKey [in]

Size, in bytes, of the buffer pointed to by the <i>pbDerivedKey</i> parameter.

### -param pcbResult [out]

Pointer to a variable that receives the number of bytes that were copied to the buffer pointed to by the <i>pbDerivedKey</i> parameter.

### -param dwFlags [in]

Flags that modify the behavior of this function. The following value can be used with the Microsoft Primitive provider.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>BCRYPT_CAPI_AES_FLAG</dt>
</dl>
</td>
<td width="60%">
Specifies that the target algorithm is AES and that the key therefore must be double expanded.
This flag is only valid with the CAPI_KDF algorithm.

</td>
</tr>
</table>

## -returns

Returns a status code that indicates the success or failure of the function.

## -remarks

You can use the following algorithm identifiers in the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptopenalgorithmprovider">BCryptOpenAlgorithmProvider</a> function before calling <b>BCryptKeyDerivation</b>:

<ul>
<li><b>BCRYPT_CAPI_KDF_ALGORITHM</b></li>
<li><b>BCRYPT_SP800108_CTR_HMAC_ALGORITHM</b></li>
<li><b>BCRYPT_SP80056A_CONCAT_ALGORITHM</b></li>
<li><b>BCRYPT_PBKDF2_ALGORITHM</b></li>
</ul>
To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). <b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptderivekey">BCryptDeriveKey</a>



<a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptkeyderivation">NCryptKeyDerivation</a>