---
UID: NF:securitybaseapi.GetSecurityDescriptorOwner
title: GetSecurityDescriptorOwner function (securitybaseapi.h)
description: Retrieves the owner information from a security descriptor.
helpviewer_keywords: ["GetSecurityDescriptorOwner","GetSecurityDescriptorOwner function [Security]","_win32_getsecuritydescriptorowner","security.getsecuritydescriptorowner","securitybaseapi/GetSecurityDescriptorOwner"]
old-location: security\getsecuritydescriptorowner.htm
tech.root: security
ms.assetid: 58e810db-348e-430c-a61f-79f67826b60d
ms.date: 12/05/2018
ms.keywords: GetSecurityDescriptorOwner, GetSecurityDescriptorOwner function [Security], _win32_getsecuritydescriptorowner, security.getsecuritydescriptorowner, securitybaseapi/GetSecurityDescriptorOwner
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
 - GetSecurityDescriptorOwner
 - securitybaseapi/GetSecurityDescriptorOwner
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
 - GetSecurityDescriptorOwner
---

# GetSecurityDescriptorOwner function


## -description

The <b>GetSecurityDescriptorOwner</b> function retrieves the owner information from a <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a>.

## -parameters

### -param pSecurityDescriptor [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure whose owner information the function retrieves.

### -param pOwner [out]

A pointer to a pointer to a 
<a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) that identifies the owner when the function returns. If the security descriptor does not contain an owner, the function sets the pointer pointed to by <i>pOwner</i> to <b>NULL</b> and ignores the remaining output parameter, <i>lpbOwnerDefaulted</i>. If the security descriptor contains an owner, the function sets the pointer pointed to by <i>pOwner</i> to the address of the security descriptor's owner SID and provides a valid value for the variable pointed to by <i>lpbOwnerDefaulted</i>.

### -param lpbOwnerDefaulted [out]

A pointer to a flag that is set to the value of the SE_OWNER_DEFAULTED flag in the 
<a href="/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a> structure when the function returns. If the value stored in the variable pointed to by the <i>pOwner</i> parameter is <b>NULL</b>, no value is set.

## -returns

If the function succeeds, the function returns nonzero.
      

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol">GetSecurityDescriptorControl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl">GetSecurityDescriptorDacl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup">GetSecurityDescriptorGroup</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorlength">GetSecurityDescriptorLength</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl">GetSecurityDescriptorSacl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsecuritydescriptor">IsValidSecurityDescriptor</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner">SetSecurityDescriptorOwner</a>