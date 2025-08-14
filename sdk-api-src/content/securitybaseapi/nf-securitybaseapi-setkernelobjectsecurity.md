---
UID: NF:securitybaseapi.SetKernelObjectSecurity
title: SetKernelObjectSecurity function (securitybaseapi.h)
description: Sets the security of a kernel object.
helpviewer_keywords: ["SetKernelObjectSecurity","SetKernelObjectSecurity function [Security]","_win32_setkernelobjectsecurity","security.setkernelobjectsecurity","securitybaseapi/SetKernelObjectSecurity"]
old-location: security\setkernelobjectsecurity.htm
tech.root: security
ms.assetid: 2a70483e-245d-4bc7-b90a-58d143364ce1
ms.date: 12/05/2018
ms.keywords: SetKernelObjectSecurity, SetKernelObjectSecurity function [Security], _win32_setkernelobjectsecurity, security.setkernelobjectsecurity, securitybaseapi/SetKernelObjectSecurity
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
 - SetKernelObjectSecurity
 - securitybaseapi/SetKernelObjectSecurity
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
 - SetKernelObjectSecurity
---

# SetKernelObjectSecurity function


## -description

The <b>SetKernelObjectSecurity</b> function sets the security of a kernel object. For example, this can be a <a href="/windows/desktop/SecGloss/p-gly">process</a>, thread, or event.<div class="alert"><b>Note</b>  This function should not be used when setting a security descriptor on file system objects. Instead, use the <a href="/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo">SetSecurityInfo</a> or <a href="/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa">SetNamedSecurityInfo</a> functions.</div>
<div> </div>

## -parameters

### -param Handle [in]

A handle to a kernel object for which security information is set.

### -param SecurityInformation [in]

A set of 
bit flags that indicate the type of security information to set. This parameter can be a combination of the 
<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> bit flags.

### -param SecurityDescriptor [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure that contains the new security information.

## -returns

If the function succeeds, the function returns nonzero.
      

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity">GetKernelObjectSecurity</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setfilesecuritya">SetFileSecurity</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity">SetPrivateObjectSecurity</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity">SetUserObjectSecurity</a>