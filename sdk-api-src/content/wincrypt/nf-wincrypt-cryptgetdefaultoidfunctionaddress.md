---
UID: NF:wincrypt.CryptGetDefaultOIDFunctionAddress
title: CryptGetDefaultOIDFunctionAddress function (wincrypt.h)
description: The CryptGetDefaultOIDFunctionAddress function loads the DLL that contains a default function address.
helpviewer_keywords: ["CryptGetDefaultOIDFunctionAddress","CryptGetDefaultOIDFunctionAddress function [Security]","_crypto2_cryptgetdefaultoidfunctionaddress","security.cryptgetdefaultoidfunctionaddress","wincrypt/CryptGetDefaultOIDFunctionAddress"]
old-location: security\cryptgetdefaultoidfunctionaddress.htm
tech.root: security
ms.assetid: 3977368c-ad13-43f9-859b-10c7f170f482
ms.date: 12/05/2018
ms.keywords: CryptGetDefaultOIDFunctionAddress, CryptGetDefaultOIDFunctionAddress function [Security], _crypto2_cryptgetdefaultoidfunctionaddress, security.cryptgetdefaultoidfunctionaddress, wincrypt/CryptGetDefaultOIDFunctionAddress
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptGetDefaultOIDFunctionAddress
 - wincrypt/CryptGetDefaultOIDFunctionAddress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptGetDefaultOIDFunctionAddress
---

# CryptGetDefaultOIDFunctionAddress function


## -description

The <b>CryptGetDefaultOIDFunctionAddress</b> function loads the DLL that contains a default function address. It can also return the address of the first or next installed default <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) function in an initialized function set and load the DLL that contains the address  of that function.

## -parameters

### -param hFuncSet [in]

Function set handle previously obtained from a call to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptinitoidfunctionset">CryptInitOIDFunctionSet</a>.

### -param dwEncodingType [in]

Encoding type to be matched. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are being used; however, additional encoding types may be added in the future. To match both current encoding types, use:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

### -param pwszDll [in, optional]

Name of the DLL to load. Normally, the DLL name is obtained from the list returned by 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetdefaultoiddlllist">CryptGetDefaultOIDDllList</a>. If <i>pwszDll</i> is <b>NULL</b>, a search is performed on the list of installed default functions.

### -param dwFlags [in]

Reserved for future use and must be zero.

### -param ppvFuncAddr [out]

A pointer to the address of the return function. If the function fails, a <b>NULL</b> is returned in <i>ppvFuncAddr</i>.

### -param phFuncAddr [in, out]

Used only if <i>pwszDll</i> is <b>NULL</b>. On the first call to the function, *<i>phFuncAddr</i> must be <b>NULL</b> to acquire the first installed function. 




When this function is successful, *<i>phFuncAddr</i> is set to a function handle. The <a href="/windows/desktop/SecGloss/r-gly">reference count</a> for the function handle is incremented.

After the first call to the function, <i>phFuncAddr</i> is set to the pointer returned by the previous call. This input pointer is always freed within the function through a call to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress">CryptFreeOIDFunctionAddress</a> by this function. The call to free the pointer is always made even when the main function returns an error.

A non-<b>NULL</b><i>phFuncAddr</i> must be released either through a call to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress">CryptFreeOIDFunctionAddress</a> or by being passed back as input to this function or as input to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetoidfunctionaddress">CryptGetOIDFunctionAddress</a>.

If <i>pwszDll</i> is not <b>NULL</b>, the value of this parameter is ignored and a non-<b>NULL</b> pointer is not freed.

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>).

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">OID Support Functions</a>