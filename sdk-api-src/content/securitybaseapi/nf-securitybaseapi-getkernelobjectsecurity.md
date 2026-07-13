---
UID: NF:securitybaseapi.GetKernelObjectSecurity
title: GetKernelObjectSecurity function (securitybaseapi.h)
description: Retrieves a copy of the security descriptor that protects a kernel object.
helpviewer_keywords: ["GetKernelObjectSecurity","GetKernelObjectSecurity function [Security]","_win32_getkernelobjectsecurity","security.getkernelobjectsecurity","securitybaseapi/GetKernelObjectSecurity"]
old-location: security\getkernelobjectsecurity.htm
tech.root: security
ms.assetid: 276e9657-5729-48cb-9531-14bfd08b7868
ms.date: 12/05/2018
ms.keywords: GetKernelObjectSecurity, GetKernelObjectSecurity function [Security], _win32_getkernelobjectsecurity, security.getkernelobjectsecurity, securitybaseapi/GetKernelObjectSecurity
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
 - GetKernelObjectSecurity
 - securitybaseapi/GetKernelObjectSecurity
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
 - GetKernelObjectSecurity
---

# GetKernelObjectSecurity function


## -description

The <b>GetKernelObjectSecurity</b> function retrieves a copy of the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> that protects a kernel object.

## -parameters

### -param Handle [in]

A handle to a kernel object.

### -param RequestedInformation [in]

Specifies a 
<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> value that identifies the security information being requested.

### -param pSecurityDescriptor [out, optional]

A pointer to a buffer the function fills with a copy of the security descriptor of the specified object. The calling <a href="/windows/desktop/SecGloss/p-gly">process</a> must have the right to view the specified aspects of the object's security status. The 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure is returned in <a href="/windows/desktop/SecGloss/s-gly">self-relative</a> format.

### -param nLength [in]

Specifies the size, in bytes, of the buffer pointed to by the <i>pSecurityDescriptor</i> parameter.

### -param lpnLengthNeeded [out]

A pointer to a variable that receives the number of bytes required for the buffer pointed to by the <i>pSecurityDescriptor</i> parameter. If this variable's value is greater than the value of the <i>nLength</i> parameter when the function returns, none of the security descriptor is copied to the buffer.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To read the owner, group, or <a href="/windows/desktop/SecGloss/d-gly">DACL</a> from the kernel object's security descriptor, the calling process must have been granted READ_CONTROL access when the handle was opened. To get READ_CONTROL access, the caller must be the owner of the object or the object's DACL must grant the access.

To read the <a href="/windows/desktop/SecGloss/s-gly">SACL</a> from the security descriptor, the calling process must have been granted ACCESS_SYSTEM_SECURITY access when the handle was opened. The proper way to get this access is to enable the SE_SECURITY_NAME privilege in the caller's current token, open the handle for ACCESS_SYSTEM_SECURITY access, and then disable the privilege.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getfilesecuritya">GetFileSecurity</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity">GetPrivateObjectSecurity</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity">GetUserObjectSecurity</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity">SetKernelObjectSecurity</a>