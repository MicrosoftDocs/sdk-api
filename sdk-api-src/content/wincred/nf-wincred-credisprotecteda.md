---
UID: NF:wincred.CredIsProtectedA
title: CredIsProtectedA function (wincred.h)
description: Specifies whether the specified credentials are encrypted by a previous call to the CredProtect function. (ANSI)
helpviewer_keywords: ["CredIsProtectedA", "wincred/CredIsProtectedA"]
old-location: security\credisprotected.htm
tech.root: security
ms.assetid: 3c38ecf5-1288-4a50-ad17-595e9ff4aaca
ms.date: 12/05/2018
ms.keywords: CredIsProtected, CredIsProtected function [Security], CredIsProtectedA, CredIsProtectedW, security.credisprotected, wincred/CredIsProtected, wincred/CredIsProtectedA, wincred/CredIsProtectedW
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredIsProtectedW (Unicode) and CredIsProtectedA (ANSI)
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
 - CredIsProtectedA
 - wincred/CredIsProtectedA
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
 - CredIsProtected
 - CredIsProtectedA
 - CredIsProtectedW
---

# CredIsProtectedA function


## -description

 The <b>CredIsProtected</b> function specifies whether the specified credentials are encrypted by a previous call to the <a href="/windows/desktop/api/wincred/nf-wincred-credprotecta">CredProtect</a> function.

## -parameters

### -param pszProtectedCredentials [in]

A pointer to a null-terminated string that specifies the credentials to test.

### -param pProtectionType [out]

A pointer to a value from the <a href="/windows/desktop/api/wincred/ne-wincred-cred_protection_type">CRED_PROTECTION_TYPE</a> enumeration that specifies whether the credentials specified in the <i>pszProtectedCredentials</i> parameter are protected.

## -returns

<b>TRUE</b> if the function succeeds; otherwise, <b>FALSE</b>.

For extended error information, call the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

> [!NOTE]
> The wincred.h header defines CredIsProtected as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
