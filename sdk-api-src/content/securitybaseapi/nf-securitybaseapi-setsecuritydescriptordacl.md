---
UID: NF:securitybaseapi.SetSecurityDescriptorDacl
title: SetSecurityDescriptorDacl function (securitybaseapi.h)
description: Sets information in a discretionary access control list (DACL). If a DACL is already present in the security descriptor, the DACL is replaced.
helpviewer_keywords: ["SetSecurityDescriptorDacl","SetSecurityDescriptorDacl function [Security]","_win32_setsecuritydescriptordacl","security.setsecuritydescriptordacl","securitybaseapi/SetSecurityDescriptorDacl"]
old-location: security\setsecuritydescriptordacl.htm
tech.root: security
ms.assetid: a873b803-391e-47e1-af7e-6dad7195968c
ms.date: 12/05/2018
ms.keywords: SetSecurityDescriptorDacl, SetSecurityDescriptorDacl function [Security], _win32_setsecuritydescriptordacl, security.setsecuritydescriptordacl, securitybaseapi/SetSecurityDescriptorDacl
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
 - SetSecurityDescriptorDacl
 - securitybaseapi/SetSecurityDescriptorDacl
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
 - SetSecurityDescriptorDacl
---

# SetSecurityDescriptorDacl function


## -description

The <b>SetSecurityDescriptorDacl</b> function sets information in a <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL). If a DACL is already present in the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a>, the DACL is replaced.

## -parameters

### -param pSecurityDescriptor [in, out]

A pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure to which the function adds the DACL. This security descriptor must be in <a href="/windows/desktop/SecGloss/a-gly">absolute</a> format, meaning that its members must be pointers to other structures, rather than offsets to contiguous data.

### -param bDaclPresent [in]

A flag that indicates the presence of a DACL in the security descriptor. If this parameter is <b>TRUE</b>, the function sets the SE_DACL_PRESENT flag in the 
<a href="/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a> structure and uses the values in the <i>pDacl</i> and <i>bDaclDefaulted</i> parameters. If this parameter is <b>FALSE</b>, the function clears the SE_DACL_PRESENT flag, and <i>pDacl</i> and <i>bDaclDefaulted</i> are ignored.

### -param pDacl [in, optional]

A pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> structure that specifies the DACL for the security descriptor. If this parameter is <b>NULL</b>, a <b>NULL</b> DACL is assigned to the security descriptor, which allows all access to the object. The DACL is referenced by, not copied into, the security descriptor.

### -param bDaclDefaulted [in]

A flag that indicates the source of the DACL. If this flag is <b>TRUE</b>, the DACL has been retrieved by some default mechanism. If <b>FALSE</b>, the DACL has been explicitly specified by a user. The function stores this value in the SE_DACL_DEFAULTED flag of the <a href="/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a> structure. If this parameter is not specified, the SE_DACL_DEFAULTED flag is cleared.

## -returns

If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

There is an important difference between an empty and a nonexistent DACL. When a DACL is empty, it contains no <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs); therefore, no access rights are explicitly granted. As a result, access to the object is implicitly denied.

When an object has no DACL (when the <i>pDacl</i> parameter is <b>NULL</b>), no protection is assigned to the object, and all access requests are granted. To help maintain security, restrict access by using a DACL.

There are three possible outcomes in different configurations of the <i>bDaclPresent</i> flag and the <i>pDacl</i> parameter:

<ul>
<li>When the <i>pDacl</i> parameter points to a DACL and the <i>bDaclPresent</i> flag is <b>TRUE</b>, a DACL is specified and it must contain access-allowed ACEs to allow access to the object.</li>
<li>When the <i>pDacl</i> parameter does not point to a DACL and the <i>bDaclPresent</i> flag is <b>TRUE</b>, a <b>NULL</b> DACL is specified. All access is allowed. You should not use a <b>NULL</b> DACL with an object because any user can change the DACL and owner of the security descriptor. This will interfere with use of the object.</li>
<li>When the <i>pDacl</i> parameter does not point to a DACL and the <i>bDaclPresent</i> flag is <b>FALSE</b>, a DACL can be provided for the object through an inheritance or default mechanism.</li>
</ul>

#### Examples

For an example that uses this function, see <a href="/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--">Creating a Security Descriptor for a New Object</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl">GetSecurityDescriptorDacl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor">InitializeSecurityDescriptor</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsecuritydescriptor">IsValidSecurityDescriptor</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup">SetSecurityDescriptorGroup</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner">SetSecurityDescriptorOwner</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl">SetSecurityDescriptorSacl</a>