---
UID: NF:securitybaseapi.GetAclInformation
title: GetAclInformation function (securitybaseapi.h)
description: Retrieves information about an access control list (ACL).
helpviewer_keywords: ["GetAclInformation","GetAclInformation function [Security]","_win32_getaclinformation","security.getaclinformation","securitybaseapi/GetAclInformation"]
old-location: security\getaclinformation.htm
tech.root: security
ms.assetid: 23ef6abd-03e9-439e-ba05-629c8d61cd66
ms.date: 12/05/2018
ms.keywords: GetAclInformation, GetAclInformation function [Security], _win32_getaclinformation, security.getaclinformation, securitybaseapi/GetAclInformation
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
 - GetAclInformation
 - securitybaseapi/GetAclInformation
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
 - GetAclInformation
---

# GetAclInformation function


## -description

The <b>GetAclInformation</b> function retrieves information about an <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL).

## -parameters

### -param pAcl [in]

A pointer to an 
ACL. The function retrieves information about this ACL. If a null value is passed, the function causes an access violation.

### -param pAclInformation [out]

A pointer to a buffer to receive the requested information. The structure that is placed into the buffer depends on the information class requested in the <i>dwAclInformationClass</i> parameter.

### -param nAclInformationLength [in]

The size, in bytes, of the buffer pointed to by the <i>pAclInformation</i> parameter.

### -param dwAclInformationClass [in]

A value of the 
<a href="/windows/desktop/api/winnt/ne-winnt-acl_information_class">ACL_INFORMATION_CLASS</a> enumeration that indicates the class of information requested. This parameter can be one of two values from this enumeration:

<ul>
<li>If the value is <b>AclRevisionInformation</b>, the function fills the buffer pointed to by the <i>pAclInformation</i> parameter with an 
<a href="/windows/desktop/api/winnt/ns-winnt-acl_revision_information">ACL_REVISION_INFORMATION</a> structure.</li>
<li>If the value is <b>AclSizeInformation</b>, the function fills the buffer pointed to by the <i>pAclInformation</i> parameter with an 
<a href="/windows/desktop/api/winnt/ns-winnt-acl_size_information">ACL_SIZE_INFORMATION</a> structure.</li>
</ul>

## -returns

If the function succeeds, the function returns nonzero.
      

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/winnt/ne-winnt-acl_information_class">ACL_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-acl_revision_information">ACL_REVISION_INFORMATION</a>



<a href="/windows/desktop/api/winnt/ns-winnt-acl_size_information">ACL_SIZE_INFORMATION</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getace">GetAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializeacl">InitializeAcl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidacl">IsValidAcl</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setaclinformation">SetAclInformation</a>