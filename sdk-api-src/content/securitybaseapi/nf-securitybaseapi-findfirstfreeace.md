---
UID: NF:securitybaseapi.FindFirstFreeAce
title: FindFirstFreeAce function (securitybaseapi.h)
description: Retrieves a pointer to the first free byte in an access control list (ACL).
helpviewer_keywords: ["FindFirstFreeAce","FindFirstFreeAce function [Security]","_win32_findfirstfreeace","security.findfirstfreeace","securitybaseapi/FindFirstFreeAce"]
old-location: security\findfirstfreeace.htm
tech.root: security
ms.assetid: bf770761-008a-4a35-b31f-b781d5a8622b
ms.date: 12/05/2018
ms.keywords: FindFirstFreeAce, FindFirstFreeAce function [Security], _win32_findfirstfreeace, security.findfirstfreeace, securitybaseapi/FindFirstFreeAce
req.header: securitybaseapi.h
req.include-header: Windows.h
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
 - FindFirstFreeAce
 - securitybaseapi/FindFirstFreeAce
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - FindFirstFreeAce
---

# FindFirstFreeAce function


## -description

The <b>FindFirstFreeAce</b> function retrieves a pointer to the first free byte in an <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL).

## -parameters

### -param pAcl [in]

A pointer to an 
ACL.

### -param pAce [out]

The address of a pointer to the first free position in the ACL created when the function returns. If the ACL is not valid, this parameter is <b>NULL</b>. If the ACL is full, this parameter points to the byte immediately following the ACL.

## -returns

If the function succeeds, the function returns nonzero.
      

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getace">GetAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getaclinformation">GetAclInformation</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>