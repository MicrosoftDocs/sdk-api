---
UID: NF:securitybaseapi.IsValidAcl
title: IsValidAcl function (securitybaseapi.h)
description: Validates an access control list (ACL).
helpviewer_keywords: ["IsValidAcl","IsValidAcl function [Security]","_win32_isvalidacl","security.isvalidacl","securitybaseapi/IsValidAcl"]
old-location: security\isvalidacl.htm
tech.root: security
ms.assetid: 3ae9f147-4e90-44df-a1af-cf6ebad92aea
ms.date: 12/05/2018
ms.keywords: IsValidAcl, IsValidAcl function [Security], _win32_isvalidacl, security.isvalidacl, securitybaseapi/IsValidAcl
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
 - IsValidAcl
 - securitybaseapi/IsValidAcl
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
 - IsValidAcl
---

# IsValidAcl function


## -description

The <b>IsValidAcl</b> function validates an <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL).

## -parameters

### -param pAcl [in]

A pointer to an
      <a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> structure validated by this function. This value must not be <b>NULL</b>.

## -returns

If the ACL is valid, the function returns nonzero.
      

If the ACL is not valid, the function returns zero. There is no extended error information for this function; do not call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function checks the revision level of the ACL and verifies that the number of <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs) specified in the <b>AceCount</b> member of the <a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> structure fits the space specified by the <b>AclSize</b> member of the <b>ACL</b> structure.

If <i>pAcl</i> is <b>NULL</b>, the application will fail with an access violation.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getaclinformation">GetAclInformation</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializeacl">InitializeAcl</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>