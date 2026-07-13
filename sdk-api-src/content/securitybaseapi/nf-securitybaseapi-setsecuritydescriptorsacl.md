---
UID: NF:securitybaseapi.SetSecurityDescriptorSacl
title: SetSecurityDescriptorSacl function (securitybaseapi.h)
description: Sets information in a system access control list (SACL). If there is already a SACL present in the security descriptor, it is replaced.
helpviewer_keywords: ["SetSecurityDescriptorSacl","SetSecurityDescriptorSacl function [Security]","_win32_setsecuritydescriptorsacl","security.setsecuritydescriptorsacl","securitybaseapi/SetSecurityDescriptorSacl"]
old-location: security\setsecuritydescriptorsacl.htm
tech.root: security
ms.assetid: 21615b63-0619-4c0c-a1b8-88ed09a1235c
ms.date: 12/05/2018
ms.keywords: SetSecurityDescriptorSacl, SetSecurityDescriptorSacl function [Security], _win32_setsecuritydescriptorsacl, security.setsecuritydescriptorsacl, securitybaseapi/SetSecurityDescriptorSacl
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
 - SetSecurityDescriptorSacl
 - securitybaseapi/SetSecurityDescriptorSacl
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
 - SetSecurityDescriptorSacl
---

# SetSecurityDescriptorSacl function


## -description

The <b>SetSecurityDescriptorSacl</b> function sets information in a <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL). If there is already a SACL present in the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a>, it is replaced.

## -parameters

### -param pSecurityDescriptor [in, out]

A pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure to which the function adds the SACL. This security descriptor must be in absolute format, meaning that its members must be pointers to other structures, rather than offsets to contiguous data.

### -param bSaclPresent [in]

Indicates the presence of a SACL in the security descriptor. If this parameter is <b>TRUE</b>, the function sets the SE_SACL_PRESENT flag in the 
<a href="/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a> structure and uses the values in the <i>pSacl</i> and <i>bSaclDefaulted</i> parameters. If it is <b>FALSE</b>, the function does not set the SE_SACL_PRESENT flag, and <i>pSacl</i> and <i>bSaclDefaulted</i> are ignored.

### -param pSacl [in, optional]

A pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> structure that specifies the SACL for the security descriptor. If this parameter is <b>NULL</b>, a <b>NULL</b> SACL is assigned to the security descriptor. The SACL is referenced by, not copied into, the security descriptor.

### -param bSaclDefaulted [in]

Indicates the source of the SACL. If this flag is <b>TRUE</b>, the SACL has been retrieved by some default mechanism. If it is <b>FALSE</b>, the SACL has been explicitly specified by a user. The function stores this value in the SE_SACL_DEFAULTED flag of the <a href="/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a> structure. If this parameter is not specified, the SE_SACL_DEFAULTED flag is cleared.

## -returns

If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl">GetSecurityDescriptorSacl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor">InitializeSecurityDescriptor</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsecuritydescriptor">IsValidSecurityDescriptor</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl">SetSecurityDescriptorDacl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup">SetSecurityDescriptorGroup</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner">SetSecurityDescriptorOwner</a>