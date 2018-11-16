---
UID: NF:securitybaseapi.SetKernelObjectSecurity
title: SetKernelObjectSecurity function
author: windows-sdk-content
description: Sets the security of a kernel object.
old-location: security\setkernelobjectsecurity.htm
tech.root: SecAuthZ
ms.assetid: 2a70483e-245d-4bc7-b90a-58d143364ce1
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: SetKernelObjectSecurity, SetKernelObjectSecurity function [Security], _win32_setkernelobjectsecurity, security.setkernelobjectsecurity, securitybaseapi/SetKernelObjectSecurity
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
 - SetKernelObjectSecurity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SetKernelObjectSecurity
: 
---

# SetKernelObjectSecurity function


## -description


The <b>SetKernelObjectSecurity</b> function sets the security of a kernel object. For example, this can be a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a>, thread, or event.<div class="alert"><b>Note</b>  This function should not be used when setting a security descriptor on file system objects. Instead, use the <a href="https://msdn.microsoft.com/f1781ba9-81eb-46f9-b530-c390b67d65de">SetSecurityInfo</a> or <a href="https://msdn.microsoft.com/70fbba50-2576-4857-a955-119fb12bf7b6">SetNamedSecurityInfo</a> functions.</div>
<div> </div>



## -parameters




### -param Handle [in]

A handle to a kernel object for which security information is set.


### -param SecurityInformation [in]

A set of 
bit flags that indicate the type of security information to set. This parameter can be a combination of the 
<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a> bit flags.


### -param SecurityDescriptor [in]

A pointer to a 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure that contains the new security information.


## -returns



If the function succeeds, the function returns nonzero.
      

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/276e9657-5729-48cb-9531-14bfd08b7868">GetKernelObjectSecurity</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="authorization_functions.htm">Low-level Access Control Functions</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a>



<a href="https://msdn.microsoft.com/27766c97-7ac5-40fc-b798-7cd07e496c0d">SetFileSecurity</a>



<a href="https://msdn.microsoft.com/726994c8-7813-4f1a-b7d7-a25e79202c33">SetPrivateObjectSecurity</a>



<a href="https://msdn.microsoft.com/219e41b8-9ac7-4747-a585-b6b9df6a1c9c">SetUserObjectSecurity</a>
 

 

