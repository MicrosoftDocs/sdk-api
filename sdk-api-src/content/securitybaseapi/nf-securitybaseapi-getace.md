---
UID: NF:securitybaseapi.GetAce
title: GetAce function (securitybaseapi.h)
description: Obtains a pointer to an access control entry (ACE) in an access control list (ACL).
helpviewer_keywords: ["GetAce","GetAce function [Security]","_win32_getace","security.getace","securitybaseapi/GetAce"]
old-location: security\getace.htm
tech.root: security
ms.assetid: 5b5d8751-20d7-40a2-bd70-cfbe956aaa03
ms.date: 12/05/2018
ms.keywords: GetAce, GetAce function [Security], _win32_getace, security.getace, securitybaseapi/GetAce
req.header: securitybaseapi.h
req.include-header: Windows.h
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
 - GetAce
 - securitybaseapi/GetAce
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
 - GetAce
---

# GetAce function


## -description

The <b>GetAce</b> function obtains a pointer to an <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) in an <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL).

## -parameters

### -param pAcl [in]

A pointer to an 
ACL that contains the ACE to be retrieved.

### -param dwAceIndex [in]

The index of the ACE to be retrieved. A value of zero corresponds to the first ACE in the ACL, a value of one to the second ACE, and so on.

### -param pAce [out]

A pointer to a pointer that the function sets to the address of the ACE.

## -returns

If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace">AddAccessAllowedAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedace">AddAccessDeniedAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addace">AddAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addauditaccessace">AddAuditAccessAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getaclinformation">GetAclInformation</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializeacl">InitializeAcl</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>