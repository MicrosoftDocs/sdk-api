---
UID: NF:wincrypt.CryptReleaseContext
title: CryptReleaseContext function (wincrypt.h)
description: Releases the handle of a cryptographic service provider (CSP) and a key container.
helpviewer_keywords: ["CryptReleaseContext","CryptReleaseContext function [Security]","_crypto2_cryptreleasecontext","security.cryptreleasecontext","wincrypt/CryptReleaseContext"]
old-location: security\cryptreleasecontext.htm
tech.root: security
ms.assetid: c1e3e708-b543-4e87-8638-a9946a83e614
ms.date: 12/05/2018
ms.keywords: CryptReleaseContext, CryptReleaseContext function [Security], _crypto2_cryptreleasecontext, security.cryptreleasecontext, wincrypt/CryptReleaseContext
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - CryptReleaseContext
 - wincrypt/CryptReleaseContext
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
 - CryptReleaseContext
---

# CryptReleaseContext function


## -description

<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptReleaseContext</b> function releases the handle of a <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) and a <a href="/windows/desktop/SecGloss/k-gly">key container</a>. At each call to this function, the <a href="/windows/desktop/SecGloss/r-gly">reference count</a> on the CSP is reduced by one. When the reference count reaches zero, the <a href="/windows/desktop/SecGloss/c-gly">context</a> is fully released and it can no longer be used by any function in the application.

An application calls this function after finishing the use of the CSP. After this function is called, the released CSP handle is no longer valid. This function does not destroy <a href="/windows/desktop/SecGloss/k-gly">key containers</a> or <a href="/windows/desktop/SecGloss/k-gly">key pairs</a>.

## -parameters

### -param hProv [in]

Handle of a cryptographic service provider (CSP) created by a call to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>.

### -param dwFlags [in]

Reserved for future use and must be zero. If <i>dwFlags</i> is not set to zero, this function returns <b>FALSE</b> but the CSP is released.

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Some possible error codes are listed in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The CSP <a href="/windows/desktop/SecGloss/c-gly">context</a> specified by <i>hProv</i> is currently being used by another <a href="/windows/desktop/SecGloss/p-gly">process</a>.

</td>
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
<dt><b>NTE_BAD_UID</b></dt>
</dl>
</td>
<td width="60%">
The <i>hProv</i> parameter does not contain a valid context handle.

</td>
</tr>
</table>

## -remarks

After this function has been called, the CSP session is finished and all existing session keys and <a href="/windows/desktop/SecGloss/h-gly">hash objects</a> created by using the <i>hProv</i> handle are no longer valid. In practice, all of these objects should be destroyed with calls to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdestroykey">CryptDestroyKey</a> and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdestroyhash">CryptDestroyHash</a> before <b>CryptReleaseContext</b> is called.


#### Examples

For an example that uses this function, see <a href="/windows/desktop/SecCrypto/example-c-program-creating-and-hashing-a-session-key">Example C Program: Creating and Hashing a Session Key</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdestroyhash">CryptDestroyHash</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdestroykey">CryptDestroyKey</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Service Provider Functions</a>