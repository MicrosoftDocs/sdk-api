---
UID: NF:wincrypt.CryptFreeOIDFunctionAddress
title: CryptFreeOIDFunctionAddress function (wincrypt.h)
description: The CryptFreeOIDFunctionAddress function releases a handle returned by CryptGetOIDFunctionAddress or CryptGetDefaultOIDFunctionAddress by decrementing the reference count on the function handle.
helpviewer_keywords: ["CryptFreeOIDFunctionAddress","CryptFreeOIDFunctionAddress function [Security]","_crypto2_cryptfreeoidfunctionaddress","security.cryptfreeoidfunctionaddress","wincrypt/CryptFreeOIDFunctionAddress"]
old-location: security\cryptfreeoidfunctionaddress.htm
tech.root: security
ms.assetid: cacacff3-25b7-4ed4-885b-b4b0b326628f
ms.date: 12/05/2018
ms.keywords: CryptFreeOIDFunctionAddress, CryptFreeOIDFunctionAddress function [Security], _crypto2_cryptfreeoidfunctionaddress, security.cryptfreeoidfunctionaddress, wincrypt/CryptFreeOIDFunctionAddress
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
 - CryptFreeOIDFunctionAddress
 - wincrypt/CryptFreeOIDFunctionAddress
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
 - CryptFreeOIDFunctionAddress
---

# CryptFreeOIDFunctionAddress function


## -description

The <b>CryptFreeOIDFunctionAddress</b> function releases a handle returned by 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetoidfunctionaddress">CryptGetOIDFunctionAddress</a> or 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress">CryptGetDefaultOIDFunctionAddress</a> by decrementing the <a href="/windows/desktop/SecGloss/r-gly">reference count</a> on the function handle. In some cases, the DLL file associated with the function is unloaded. For details, see Remarks.

## -parameters

### -param hFuncAddr [in]

Handle of the function previously obtained from a call to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetoidfunctionaddress">CryptGetOIDFunctionAddress</a> or 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress">CryptGetDefaultOIDFunctionAddress</a>.

### -param dwFlags [in]

Reserved for future use and must be zero.

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>).

## -remarks

If the <a href="/windows/desktop/SecGloss/r-gly">reference count</a> becomes zero and a DLL is loaded for the function being freed, the DLL might be unloaded. If the DLL exports the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow">DLLCanUnloadNow</a> function, that function is called and its return is checked. An S_FALSE return from this function cancels the unloading of the DLL at this time. If the function returns S_TRUE or if the DLL does not export the <b>DLLCanUnloadNow</b> function, an unloading process is started. In this case, actual unloading is deferred for 15 seconds. If another <b>CryptFreeOIDFunctionAddress</b> or <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress">CryptGetDefaultOIDFunctionAddress</a> that requires the DLL occurs before the 15 seconds elapse, the deferred unload process is canceled.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress">CryptGetDefaultOIDFunctionAddress</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetoidfunctionaddress">CryptGetOIDFunctionAddress</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow">DLLCanUnloadNow</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">OID Support Functions</a>