---
UID: NF:securitybaseapi.IsValidSecurityDescriptor
title: IsValidSecurityDescriptor function (securitybaseapi.h)
description: Determines whether the components of a security descriptor are valid.
helpviewer_keywords: ["IsValidSecurityDescriptor","IsValidSecurityDescriptor function [Security]","_win32_isvalidsecuritydescriptor","security.isvalidsecuritydescriptor","securitybaseapi/IsValidSecurityDescriptor"]
old-location: security\isvalidsecuritydescriptor.htm
tech.root: security
ms.assetid: 24a98229-11e4-45ef-988b-c2cf831275e7
ms.date: 12/05/2018
ms.keywords: IsValidSecurityDescriptor, IsValidSecurityDescriptor function [Security], _win32_isvalidsecuritydescriptor, security.isvalidsecuritydescriptor, securitybaseapi/IsValidSecurityDescriptor
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
 - IsValidSecurityDescriptor
 - securitybaseapi/IsValidSecurityDescriptor
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
 - IsValidSecurityDescriptor
---

# IsValidSecurityDescriptor function


## -description

The <b>IsValidSecurityDescriptor</b> function determines whether the components of a <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> are valid.

## -parameters

### -param pSecurityDescriptor [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure that the function validates.

## -returns

If the components of the security descriptor are valid, the return value is nonzero.

If any of the components of the security descriptor are not valid, the return value is zero. There is no extended error information for this function; do not call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>IsValidSecurityDescriptor</b> function checks the validity of the components that are present in the security descriptor. It does not verify whether certain components are present nor does it verify the contents of the individual ACE or ACL.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol">GetSecurityDescriptorControl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl">GetSecurityDescriptorDacl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup">GetSecurityDescriptorGroup</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorlength">GetSecurityDescriptorLength</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner">GetSecurityDescriptorOwner</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl">GetSecurityDescriptorSacl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor">InitializeSecurityDescriptor</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidacl">IsValidAcl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsid">IsValidSid</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl">SetSecurityDescriptorDacl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup">SetSecurityDescriptorGroup</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner">SetSecurityDescriptorOwner</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl">SetSecurityDescriptorSacl</a>