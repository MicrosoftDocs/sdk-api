---
UID: NF:wincrypt.CryptSetProviderExW
title: CryptSetProviderExW function (wincrypt.h)
description: Specifies the default cryptographic service provider (CSP) of a specified provider type for the local computer or current user. (Unicode)
helpviewer_keywords: ["CRYPT_DELETE_DEFAULT", "CRYPT_MACHINE_DEFAULT", "CRYPT_USER_DEFAULT", "CryptSetProviderEx", "CryptSetProviderEx function [Security]", "CryptSetProviderExW", "_crypto2_cryptsetproviderex", "security.cryptsetproviderex", "wincrypt/CryptSetProviderEx", "wincrypt/CryptSetProviderExW"]
old-location: security\cryptsetproviderex.htm
tech.root: security
ms.assetid: 5f0c2724-5144-4a22-a7da-2a5162f06f5d
ms.date: 12/05/2018
ms.keywords: CRYPT_DELETE_DEFAULT, CRYPT_MACHINE_DEFAULT, CRYPT_USER_DEFAULT, CryptSetProviderEx, CryptSetProviderEx function [Security], CryptSetProviderExA, CryptSetProviderExW, _crypto2_cryptsetproviderex, security.cryptsetproviderex, wincrypt/CryptSetProviderEx, wincrypt/CryptSetProviderExA, wincrypt/CryptSetProviderExW
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CryptSetProviderExW (Unicode) and CryptSetProviderExA (ANSI)
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
 - CryptSetProviderExW
 - wincrypt/CryptSetProviderExW
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
 - CryptSetProviderEx
 - CryptSetProviderExA
 - CryptSetProviderExW
---

# CryptSetProviderExW function


## -description

<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptSetProviderEx</b> function specifies the default <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) of a specified provider type for the local computer or current user.
<div class="alert"><b>Note</b>  Typical applications do not use this function. It is intended for use solely by administrative applications.</div><div> </div>

## -parameters

### -param pszProvName [in]

The name of the new default CSP. This must be a CSP installed on the computer. For a list of available cryptographic providers, see 
<a href="/windows/desktop/SecCrypto/cryptographic-provider-names">Cryptographic Provider Names</a>.

### -param dwProvType [in]

The provider type of the CSP specified by <i>pszProvName</i>.

### -param pdwReserved [in]

This parameter is reserved for future use and must be <b>NULL</b>.

### -param dwFlags [in]

The following flag values are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DELETE_DEFAULT"></a><a id="crypt_delete_default"></a><dl>
<dt><b>CRYPT_DELETE_DEFAULT</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Can be used in conjunction with CRYPT_MACHINE_DEFAULT or CRYPT_USER_DEFAULT to delete the default.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_USER_DEFAULT"></a><a id="crypt_user_default"></a><dl>
<dt><b>CRYPT_USER_DEFAULT</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Causes the user-context default CSP of the specified type to be set.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_MACHINE_DEFAULT"></a><a id="crypt_machine_default"></a><dl>
<dt><b>CRYPT_MACHINE_DEFAULT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Causes the computer default CSP of the specified type to be set.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Possible error codes include those shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The operating system ran out of memory.

</td>
</tr>
</table>

## -remarks

Most applications do not specify a CSP name when calling the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> function; however, an application can specify a CSP name and thereby select a CSP with an appropriate level of security. Because calls to <b>CryptSetProviderEx</b> determine the CSP of a specified type used by all applications from that point on, <b>CryptSetProviderEx</b> must never be called without a user's consent.





> [!NOTE]
> The wincrypt.h header defines CryptSetProviderEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetprovidera">CryptSetProvider</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Service Provider Functions</a>
