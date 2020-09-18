---
UID: NF:wincrypt.CryptContextAddRef
title: CryptContextAddRef function (wincrypt.h)
description: Adds one to the reference count of an HCRYPTPROV cryptographic service provider (CSP) handle.
helpviewer_keywords: ["CryptContextAddRef","CryptContextAddRef function [Security]","_crypto2_cryptcontextaddref","security.cryptcontextaddref","wincrypt/CryptContextAddRef"]
old-location: security\cryptcontextaddref.htm
tech.root: security
ms.assetid: 074666a7-369c-43bc-97d9-3bcc9703976b
ms.date: 12/05/2018
ms.keywords: CryptContextAddRef, CryptContextAddRef function [Security], _crypto2_cryptcontextaddref, security.cryptcontextaddref, wincrypt/CryptContextAddRef
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
 - CryptContextAddRef
 - wincrypt/CryptContextAddRef
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
 - CryptContextAddRef
---

# CryptContextAddRef function


## -description

<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptContextAddRef</b> function adds one to the <a href="/windows/desktop/SecGloss/r-gly">reference count</a> of an 
<a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a> <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) handle. This function should be used if the CSP handle is included as a member of any structure passed to another function. The 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptreleasecontext">CryptReleaseContext</a> function should be called when the CSP handle is no longer needed.

## -parameters

### -param hProv [in]

<a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a> handle for which the <a href="/windows/desktop/SecGloss/r-gly">reference count</a> is being incremented. This handle must have already been created using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>.

### -param pdwReserved [in]

Reserved for future use and must be <b>NULL</b>.

### -param dwFlags [in]

Reserved for future use and must be zero.

## -returns

If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (FALSE). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. One possible error code is the following.

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
</table>

## -remarks

This function increases the <a href="/windows/desktop/SecGloss/r-gly">reference count</a> on a 
<a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a> handle so that multiple calls to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptreleasecontext">CryptReleaseContext</a> are required to actually release the handle.


#### Examples

The following example increments the <a href="/windows/desktop/SecGloss/r-gly">reference count</a> on an acquired CSP handle.


```cpp
//--------------------------------------------------------------------
// hCryptProv is a HCRYPTPROV variable that was previously acquired
// by using CryptAcquireContext or CryptAcquireCertificatePrivateKey.

if(CryptContextAddRef(
       hCryptProv, 
       NULL, 
       0)) 
{
    printf("CryptContextAddRef succeeded. \n");
}
else
{
   printf("Error during CryptContextAddRef!\n");
   exit(1);
}
//--------------------------------------------------------------------
//  The reference count on hCryptProv is now greater than one. The 
//  first call to CryptReleaseContext will not release the provider 
//  handle. A second call to CryptReleaseContext would be needed to 
//  release the context.
```


For another example that uses this function, see <a href="/windows/desktop/SecCrypto/example-c-program-using-cryptacquirecontext">Example C Program: Using CryptAcquireContext</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptreleasecontext">CryptReleaseContext</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Service Provider Functions</a>