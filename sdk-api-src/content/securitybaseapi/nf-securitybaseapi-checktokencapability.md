---
UID: NF:securitybaseapi.CheckTokenCapability
title: CheckTokenCapability function (securitybaseapi.h)
description: Checks the capabilities of a given token.
helpviewer_keywords: ["CheckTokenCapability","CheckTokenCapability function [Security]","security.checktokencapability","securitybaseapi/CheckTokenCapability"]
old-location: security\checktokencapability.htm
tech.root: security
ms.assetid: 436A5110-B79E-4E64-92E8-1C9E713D0948
ms.date: 12/05/2018
ms.keywords: CheckTokenCapability, CheckTokenCapability function [Security], security.checktokencapability, securitybaseapi/CheckTokenCapability
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CheckTokenCapability
 - securitybaseapi/CheckTokenCapability
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - Kernel32.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - CheckTokenCapability
---

# CheckTokenCapability function


## -description

The <b>CheckTokenCapability</b> function checks the capabilities of a given token.

## -parameters

### -param TokenHandle [in, optional]

A handle to an access token. The handle must have TOKEN_QUERY access to the token. The token must be an <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a>. 
      

If <i>TokenHandle</i> is <b>NULL</b>, <b>CheckTokenCapability</b> uses the impersonation token of the calling thread. If the thread is not impersonating, the function duplicates the thread's <a href="/windows/desktop/SecGloss/p-gly">primary token</a> to create an <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a>.

### -param CapabilitySidToCheck [in]

A pointer to a capability <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure. The <b>CheckTokenCapability</b> function checks the capabilities of this access token.

### -param HasCapability [out]

Receives the results of the check. If the access token has the capability, it returns <b>TRUE</b>, otherwise, it returns <b>FALSE</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>