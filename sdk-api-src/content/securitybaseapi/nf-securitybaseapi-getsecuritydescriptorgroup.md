---
UID: NF:securitybaseapi.GetSecurityDescriptorGroup
title: GetSecurityDescriptorGroup function (securitybaseapi.h)
description: Retrieves the primary group information from a security descriptor.
helpviewer_keywords: ["GetSecurityDescriptorGroup","GetSecurityDescriptorGroup function [Security]","_win32_getsecuritydescriptorgroup","security.getsecuritydescriptorgroup","securitybaseapi/GetSecurityDescriptorGroup"]
old-location: security\getsecuritydescriptorgroup.htm
tech.root: security
ms.assetid: a920b49e-a4c2-4e49-b529-88c12205d995
ms.date: 12/05/2018
ms.keywords: GetSecurityDescriptorGroup, GetSecurityDescriptorGroup function [Security], _win32_getsecuritydescriptorgroup, security.getsecuritydescriptorgroup, securitybaseapi/GetSecurityDescriptorGroup
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
 - GetSecurityDescriptorGroup
 - securitybaseapi/GetSecurityDescriptorGroup
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
 - GetSecurityDescriptorGroup
---

# GetSecurityDescriptorGroup function


## -description

The <b>GetSecurityDescriptorGroup</b> function retrieves the primary group information from a <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a>.

## -parameters

### -param pSecurityDescriptor [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure whose primary group information the function retrieves.

### -param pGroup [out]

A pointer to a pointer to a 
<a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) that identifies the primary group when the function returns. If the security descriptor does not contain a primary group, the function sets the pointer pointed to by <i>pGroup</i> to <b>NULL</b> and ignores the remaining output parameter, <i>lpbGroupDefaulted</i>. If the security descriptor contains a primary group, the function sets the pointer pointed to by <i>pGroup</i> to the address of the security descriptor's group SID and provides a valid value for the variable pointed to by <i>lpbGroupDefaulted</i>.

### -param lpbGroupDefaulted [out]

A pointer to a flag that is set to the value of the SE_GROUP_DEFAULTED flag in the 
<a href="/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a> structure when the function returns. If the value stored in the variable pointed to by the <i>pGroup</i> parameter is <b>NULL</b>, no value is set.

## -returns

If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol">GetSecurityDescriptorControl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl">GetSecurityDescriptorDacl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorlength">GetSecurityDescriptorLength</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner">GetSecurityDescriptorOwner</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl">GetSecurityDescriptorSacl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsecuritydescriptor">IsValidSecurityDescriptor</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup">SetSecurityDescriptorGroup</a>