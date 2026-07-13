---
UID: NF:securitybaseapi.GetSecurityDescriptorSacl
title: GetSecurityDescriptorSacl function (securitybaseapi.h)
description: Retrieves a pointer to the system access control list (SACL) in a specified security descriptor.
helpviewer_keywords: ["GetSecurityDescriptorSacl","GetSecurityDescriptorSacl function [Security]","_win32_getsecuritydescriptorsacl","security.getsecuritydescriptorsacl","securitybaseapi/GetSecurityDescriptorSacl"]
old-location: security\getsecuritydescriptorsacl.htm
tech.root: security
ms.assetid: 6bf59735-aaa3-4751-8c98-00cc197df4e5
ms.date: 12/05/2018
ms.keywords: GetSecurityDescriptorSacl, GetSecurityDescriptorSacl function [Security], _win32_getsecuritydescriptorsacl, security.getsecuritydescriptorsacl, securitybaseapi/GetSecurityDescriptorSacl
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
 - GetSecurityDescriptorSacl
 - securitybaseapi/GetSecurityDescriptorSacl
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
 - GetSecurityDescriptorSacl
---

# GetSecurityDescriptorSacl function


## -description

The <b>GetSecurityDescriptorSacl</b> function retrieves a pointer to the <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) in a specified <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a>.

## -parameters

### -param pSecurityDescriptor [in]

A pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure that contains the SACL to which the function retrieves a pointer.

### -param lpbSaclPresent [out]

A pointer to a flag the function sets to indicate the presence of a SACL in the specified security descriptor. If this parameter is <b>TRUE</b>, the security descriptor contains a SACL, and the remaining output parameters in this function receive valid values. If this parameter is <b>FALSE</b>, the security descriptor does not contain a SACL, and the remaining output parameters do not receive valid values.

### -param pSacl [out]

A pointer to a pointer to an 
<a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL). If a SACL exists, the function sets the pointer pointed to by <i>pSacl</i> to the address of the security descriptor's SACL. If a SACL does not exist, no value is stored. 




If the function stores a <b>NULL</b> value in the pointer pointed to by <i>pSacl</i>, the security descriptor has a <b>NULL</b> SACL.

### -param lpbSaclDefaulted [out]

A pointer to a flag that is set to the value of the SE_SACL_DEFAULTED flag in the 
<a href="/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a> structure if a SACL exists for the security descriptor.

## -returns

If the function succeeds, the function returns nonzero.
      

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol">GetSecurityDescriptorControl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl">GetSecurityDescriptorDacl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup">GetSecurityDescriptorGroup</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorlength">GetSecurityDescriptorLength</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner">GetSecurityDescriptorOwner</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor">InitializeSecurityDescriptor</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsecuritydescriptor">IsValidSecurityDescriptor</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl">SetSecurityDescriptorSacl</a>