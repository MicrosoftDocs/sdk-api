---
UID: NF:wincrypt.CryptUninstallDefaultContext
title: CryptUninstallDefaultContext function (wincrypt.h)
description: Important  This API is deprecated. (CryptUninstallDefaultContext)
helpviewer_keywords: ["CryptUninstallDefaultContext","CryptUninstallDefaultContext function [Security]","_crypto2_cryptuninstalldefaultcontext","security.cryptuninstalldefaultcontext","wincrypt/CryptUninstallDefaultContext"]
old-location: security\cryptuninstalldefaultcontext.htm
tech.root: security
ms.assetid: ad7be5cf-f078-4a9f-81c4-959e4203dba8
ms.date: 12/05/2018
ms.keywords: CryptUninstallDefaultContext, CryptUninstallDefaultContext function [Security], _crypto2_cryptuninstalldefaultcontext, security.cryptuninstalldefaultcontext, wincrypt/CryptUninstallDefaultContext
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptUninstallDefaultContext
 - wincrypt/CryptUninstallDefaultContext
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
 - CryptUninstallDefaultContext
---

# CryptUninstallDefaultContext function


## -description

<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptUninstallDefaultContext</b> function removes a default <a href="/windows/desktop/SecGloss/c-gly">context</a> previously installed by <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptinstalldefaultcontext">CryptInstallDefaultContext</a>. This function will block until any threads currently using this context finish, if the default context was installed with CRYPT_DEFAULT_CONTEXT_PROCESS_FLAG set.

## -parameters

### -param hDefaultContext [in]

Handle of the context to be released.

### -param dwFlags [in]

Reserved for future use.

### -param pvReserved [in]

Reserved for future use.

## -returns

If the function succeeds, the return value is nonzero (TRUE) .If the function fails, the return value is zero (FALSE). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
