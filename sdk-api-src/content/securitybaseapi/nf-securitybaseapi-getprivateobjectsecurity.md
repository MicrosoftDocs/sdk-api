---
UID: NF:securitybaseapi.GetPrivateObjectSecurity
title: GetPrivateObjectSecurity function (securitybaseapi.h)
description: Retrieves information from a private object's security descriptor.
helpviewer_keywords: ["GetPrivateObjectSecurity","GetPrivateObjectSecurity function [Security]","_win32_getprivateobjectsecurity","security.getprivateobjectsecurity","securitybaseapi/GetPrivateObjectSecurity"]
old-location: security\getprivateobjectsecurity.htm
tech.root: security
ms.assetid: 3e93c0a0-e449-4df1-812b-c3fb0dfe9c19
ms.date: 12/05/2018
ms.keywords: GetPrivateObjectSecurity, GetPrivateObjectSecurity function [Security], _win32_getprivateobjectsecurity, security.getprivateobjectsecurity, securitybaseapi/GetPrivateObjectSecurity
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - GetPrivateObjectSecurity
 - securitybaseapi/GetPrivateObjectSecurity
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
 - GetPrivateObjectSecurity
---

# GetPrivateObjectSecurity function


## -description

The <b>GetPrivateObjectSecurity</b> function retrieves information from a private object's <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a>.

## -parameters

### -param ObjectDescriptor [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure. This is the security descriptor to be queried.

### -param SecurityInformation [in]

A set of bit flags that indicate the parts of the security descriptor to retrieve. This parameter can be a combination of the 
<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> bit flags.

### -param ResultantDescriptor [out, optional]

A pointer to a buffer that receives a copy of the requested information from the specified security descriptor. The 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure is returned in <a href="/windows/desktop/SecGloss/s-gly">self-relative</a> format.

### -param DescriptorLength [in]

Specifies the size, in bytes, of the buffer pointed to by the <i>ResultantDescriptor</i> parameter.

### -param ReturnLength [out]

A pointer to a variable the function sets to zero if the descriptor is copied successfully. If the buffer is too small for the security descriptor, this variable receives the number of bytes required. If this variable's value is greater than the value of the <i>DescriptorLength</i> parameter when the function returns, the function returns <b>FALSE</b> and none of the security descriptor is copied to the buffer.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function is intended for use by resource managers only. To implement the standard access control semantics for updating security descriptors, a resource manager should verify that the following conditions are met before calling <b>GetPrivateObjectSecurity</b>:

<ul>
<li>If the object's owner is being set, the calling <a href="/windows/desktop/SecGloss/p-gly">process</a> must have either WRITE_OWNER permission or be the object's owner.</li>
<li>If the object's <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> is being set, the calling process must have either WRITE_DAC permission or be the object's owner.</li>
<li>If the object's <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> is being set, the SE_SECURITY_NAME privilege must be enabled for the calling process.</li>
</ul>
If the preceding conditions are not met, a call to this function does not fail, however, standard access policy is not enforced.

## -see-also

<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control Overview</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity">CreatePrivateObjectSecurity</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity">DestroyPrivateObjectSecurity</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfilesecuritya">GetFileSecurity</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity">GetKernelObjectSecurity</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity">GetUserObjectSecurity</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity">SetPrivateObjectSecurity</a>