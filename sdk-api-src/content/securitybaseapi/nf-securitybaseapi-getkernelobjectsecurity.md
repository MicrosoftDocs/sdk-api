---
UID: NF:securitybaseapi.GetKernelObjectSecurity
title: GetKernelObjectSecurity function
author: windows-sdk-content
description: Retrieves a copy of the security descriptor that protects a kernel object.
old-location: security\getkernelobjectsecurity.htm
tech.root: secauthz
ms.assetid: 276e9657-5729-48cb-9531-14bfd08b7868
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: GetKernelObjectSecurity, GetKernelObjectSecurity function [Security], _win32_getkernelobjectsecurity, security.getkernelobjectsecurity, securitybaseapi/GetKernelObjectSecurity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetKernelObjectSecurity
: 
---

# GetKernelObjectSecurity function


## -description


The <b>GetKernelObjectSecurity</b> function retrieves a copy of the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> that protects a kernel object.


## -parameters




### -param Handle [in]

A handle to a kernel object.


### -param RequestedInformation [in]

Specifies a 
<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a> value that identifies the security information being requested.


### -param pSecurityDescriptor [out, optional]

A pointer to a buffer the function fills with a copy of the security descriptor of the specified object. The calling <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a> must have the right to view the specified aspects of the object's security status. The 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure is returned in <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">self-relative</a> format.


### -param nLength [in]

Specifies the size, in bytes, of the buffer pointed to by the <i>pSecurityDescriptor</i> parameter.


### -param lpnLengthNeeded [out]

A pointer to a variable that receives the number of bytes required for the buffer pointed to by the <i>pSecurityDescriptor</i> parameter. If this variable's value is greater than the value of the <i>nLength</i> parameter when the function returns, none of the security descriptor is copied to the buffer.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To read the owner, group, or <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">DACL</a> from the kernel object's security descriptor, the calling process must have been granted READ_CONTROL access when the handle was opened. To get READ_CONTROL access, the caller must be the owner of the object or the object's DACL must grant the access.

To read the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">SACL</a> from the security descriptor, the calling process must have been granted ACCESS_SYSTEM_SECURITY access when the handle was opened. The proper way to get this access is to enable the SE_SECURITY_NAME privilege in the caller's current token, open the handle for ACCESS_SYSTEM_SECURITY access, and then disable the privilege.




## -see-also




<a href="https://msdn.microsoft.com/4043b76b-76b9-4111-8a29-a808b2412be0">GetFileSecurity</a>



<a href="https://msdn.microsoft.com/3e93c0a0-e449-4df1-812b-c3fb0dfe9c19">GetPrivateObjectSecurity</a>



<a href="https://msdn.microsoft.com/998c2520-7833-4efd-a794-b13b528f0485">GetUserObjectSecurity</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="authorization_functions.htm">Low-level Access Control Functions</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a>



<a href="https://msdn.microsoft.com/2a70483e-245d-4bc7-b90a-58d143364ce1">SetKernelObjectSecurity</a>
 

 

