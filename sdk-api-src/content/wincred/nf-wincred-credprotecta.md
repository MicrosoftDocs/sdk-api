---
UID: NF:wincred.CredProtectA
title: CredProtectA function (wincred.h)
description: Encrypts the specified credentials so that only the current security context can decrypt them. (ANSI)
helpviewer_keywords: ["CredProtectA", "wincred/CredProtectA"]
old-location: security\credprotect.htm
tech.root: security
ms.assetid: 1e299dfb-2ffe-463c-9e2c-b7774a2216e3
ms.date: 12/05/2018
ms.keywords: CredProtect, CredProtect function [Security], CredProtectA, CredProtectW, security.credprotect, wincred/CredProtect, wincred/CredProtectA, wincred/CredProtectW
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredProtectW (Unicode) and CredProtectA (ANSI)
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
 - CredProtectA
 - wincred/CredProtectA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-advapi32-l2-1-0.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - sechost.dll
 - API-MS-Win-Security-credentials-l1-1-0.dll
api_name:
 - CredProtect
 - CredProtectA
 - CredProtectW
---

# CredProtectA function


## -description

The <b>CredProtect</b> function encrypts the specified credentials so that only the current security context can decrypt them.

## -parameters

### -param fAsSelf [in]

Set to <b>TRUE</b> to specify that the credentials are encrypted in the security context of the current process. Set to <b>FALSE</b> to specify that credentials are encrypted in the security context of the calling thread security context.

### -param pszCredentials [in]

A pointer to a string that specifies the credentials to encrypt. The function encrypts the number of characters provided in the <i>cchCredentials</i> parameter.

### -param cchCredentials [in]

The size, in characters, of the <i>pszCredentials</i> buffer.

### -param pszProtectedCredentials [out]

A pointer to a string that, on output, receives the encrypted credentials.

### -param pcchMaxChars [in, out]

The size, in characters of the <i>pszProtectedCredentials</i> buffer. On output, if the <i>pszProtectedCredentials</i> is not of sufficient size to receive the encrypted credentials, this parameter specifies the required size, in characters, of the <i>pszProtectedCredentials</i> buffer.

### -param ProtectionType [out]

A pointer to a <a href="/windows/desktop/api/wincred/ne-wincred-cred_protection_type">CRED_PROTECTION_TYPE</a> enumeration type that, on output, specifies the type of protection provided.

## -returns

<b>TRUE</b> if the function succeeds; otherwise, <b>FALSE</b>.

For extended error information, call the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

Note that the output of the <b>CredProtect</b> function is not integrity protected, so if the output is modified, the <a href="/windows/desktop/api/wincred/nf-wincred-credunprotecta">CredUnprotect</a> function is not updated and may produce incorrect results.




> [!NOTE]
> The wincred.h header defines CredProtect as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
