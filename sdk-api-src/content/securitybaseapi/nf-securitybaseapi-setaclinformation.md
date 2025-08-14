---
UID: NF:securitybaseapi.SetAclInformation
title: SetAclInformation function (securitybaseapi.h)
description: Sets information about an access control list (ACL).
helpviewer_keywords: ["SetAclInformation","SetAclInformation function [Security]","_win32_setaclinformation","security.setaclinformation","securitybaseapi/SetAclInformation"]
old-location: security\setaclinformation.htm
tech.root: security
ms.assetid: bb4dd7f9-2f15-4a27-89c9-1675f4fb8d92
ms.date: 12/05/2018
ms.keywords: SetAclInformation, SetAclInformation function [Security], _win32_setaclinformation, security.setaclinformation, securitybaseapi/SetAclInformation
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
 - SetAclInformation
 - securitybaseapi/SetAclInformation
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
 - SetAclInformation
---

# SetAclInformation function


## -description

The <b>SetAclInformation</b> function sets information about an <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL).

## -parameters

### -param pAcl [in, out]

A pointer to an 
ACL. The function sets information in this ACL.

### -param pAclInformation [in]

A pointer to a buffer that contains the information to be set. This must be a pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-acl_revision_information">ACL_REVISION_INFORMATION</a> structure.

### -param nAclInformationLength [in]

The size, in bytes, of the buffer pointed to by the <i>pAclInfo</i> parameter.

### -param dwAclInformationClass [in]

An 
<a href="/windows/desktop/api/winnt/ne-winnt-acl_information_class">ACL_INFORMATION_CLASS</a> enumerated type that gives the class of information requested. 




Currently, this parameter can be <b>AclRevisionInformation</b>. This means that the buffer pointed to by the <i>pAclInformation</i> parameter contains an 
<a href="/windows/desktop/api/winnt/ns-winnt-acl_revision_information">ACL_REVISION_INFORMATION</a> structure.

## -returns

If the function succeeds, the function returns nonzero.
      

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/winnt/ne-winnt-acl_information_class">ACL_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-acl_revision_information">ACL_REVISION_INFORMATION</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getaclinformation">GetAclInformation</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializeacl">InitializeAcl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidacl">IsValidAcl</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>