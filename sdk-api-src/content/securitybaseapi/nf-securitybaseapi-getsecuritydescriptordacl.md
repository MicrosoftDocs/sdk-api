---
UID: NF:securitybaseapi.GetSecurityDescriptorDacl
title: GetSecurityDescriptorDacl function (securitybaseapi.h)
description: Retrieves a pointer to the discretionary access control list (DACL) in a specified security descriptor.
helpviewer_keywords: ["GetSecurityDescriptorDacl","GetSecurityDescriptorDacl function [Security]","_win32_getsecuritydescriptordacl","security.getsecuritydescriptordacl","securitybaseapi/GetSecurityDescriptorDacl"]
old-location: security\getsecuritydescriptordacl.htm
tech.root: security
ms.assetid: 8006c8bb-4976-463f-b074-a59c3bbab36b
ms.date: 12/05/2018
ms.keywords: GetSecurityDescriptorDacl, GetSecurityDescriptorDacl function [Security], _win32_getsecuritydescriptordacl, security.getsecuritydescriptordacl, securitybaseapi/GetSecurityDescriptorDacl
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
 - GetSecurityDescriptorDacl
 - securitybaseapi/GetSecurityDescriptorDacl
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
 - GetSecurityDescriptorDacl
---

# GetSecurityDescriptorDacl function


## -description

The <b>GetSecurityDescriptorDacl</b> function retrieves a pointer to the <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) in a specified <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a>.

## -parameters

### -param pSecurityDescriptor [in]

A pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure that contains the DACL. The function retrieves a pointer to it.

### -param lpbDaclPresent [out]

A pointer to a value that indicates the presence of a DACL in the specified security descriptor. If <i>lpbDaclPresent</i> is <b>TRUE</b>, the security descriptor contains a DACL, and the remaining output parameters in this function receive valid values. If <i>lpbDaclPresent</i> is <b>FALSE</b>, the security descriptor does not contain a DACL, and the remaining output parameters do not receive valid values.

A value of <b>TRUE</b> for <i>lpbDaclPresent</i> does not mean that <i>pDacl</i> is not <b>NULL</b>.  That is, <i>lpbDaclPresent</i> can be <b>TRUE</b> while <i>pDacl</i> is <b>NULL</b>, meaning that a <b>NULL</b> DACL is in effect.   A <b>NULL</b> DACL implicitly allows all access to an object and is not the same as an empty DACL. An empty DACL permits no access to an object.  For information about creating a proper DACL, see <a href="/windows/desktop/SecBP/creating-a-dacl">Creating a DACL</a>.

### -param pDacl [out]

A pointer to a pointer to an 
<a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL). If a DACL exists, the function sets the pointer pointed to by <i>pDacl</i> to the address of the security descriptor's DACL. If a DACL does not exist, no value is stored. 




If the function stores a <b>NULL</b> value in the pointer pointed to by <i>pDacl</i>, the security descriptor has a <b>NULL</b> DACL. A <b>NULL</b> DACL implicitly allows all access to an object.

If an application expects a non-<b>NULL</b> DACL but encounters a <b>NULL</b> DACL, the application should fail securely and not allow access.

### -param lpbDaclDefaulted [out]

A pointer to a flag set to the value of the SE_DACL_DEFAULTED flag in the 
<a href="/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a> structure if a DACL exists for the security descriptor. If this flag is <b>TRUE</b>, the DACL was retrieved by a default mechanism; if <b>FALSE</b>, the DACL was explicitly specified by a user.

## -returns

If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol">GetSecurityDescriptorControl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup">GetSecurityDescriptorGroup</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorlength">GetSecurityDescriptorLength</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner">GetSecurityDescriptorOwner</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl">GetSecurityDescriptorSacl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor">InitializeSecurityDescriptor</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsecuritydescriptor">IsValidSecurityDescriptor</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl">SetSecurityDescriptorDacl</a>