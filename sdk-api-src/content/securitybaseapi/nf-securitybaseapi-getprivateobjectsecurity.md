---
UID: NF:securitybaseapi.GetPrivateObjectSecurity
title: GetPrivateObjectSecurity function
author: windows-sdk-content
description: Retrieves information from a private object's security descriptor.
old-location: security\getprivateobjectsecurity.htm
tech.root: secauthz
ms.assetid: 3e93c0a0-e449-4df1-812b-c3fb0dfe9c19
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPrivateObjectSecurity, GetPrivateObjectSecurity function [Security], _win32_getprivateobjectsecurity, security.getprivateobjectsecurity, securitybaseapi/GetPrivateObjectSecurity
ms.topic: function
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
 - GetPrivateObjectSecurity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetPrivateObjectSecurity function


## -description


The <b>GetPrivateObjectSecurity</b> function retrieves information from a private object's <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a>.


## -parameters




### -param ObjectDescriptor [in]

A pointer to a 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure. This is the security descriptor to be queried.


### -param SecurityInformation [in]

A set of bit flags that indicate the parts of the security descriptor to retrieve. This parameter can be a combination of the 
<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a> bit flags.


### -param ResultantDescriptor [out, optional]

A pointer to a buffer that receives a copy of the requested information from the specified security descriptor. The 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure is returned in <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">self-relative</a> format.


### -param DescriptorLength [in]

Specifies the size, in bytes, of the buffer pointed to by the <i>ResultantDescriptor</i> parameter.


### -param ReturnLength [out]

A pointer to a variable the function sets to zero if the descriptor is copied successfully. If the buffer is too small for the security descriptor, this variable receives the number of bytes required. If this variable's value is greater than the value of the <i>DescriptorLength</i> parameter when the function returns, the function returns <b>FALSE</b> and none of the security descriptor is copied to the buffer.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function is intended for use by resource managers only. To implement the standard access control semantics for updating security descriptors, a resource manager should verify that the following conditions are met before calling <b>GetPrivateObjectSecurity</b>:

<ul>
<li>If the object's owner is being set, the calling <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a> must have either WRITE_OWNER permission or be the object's owner.</li>
<li>If the object's <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> is being set, the calling process must have either WRITE_DAC permission or be the object's owner.</li>
<li>If the object's <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> is being set, the SE_SECURITY_NAME privilege must be enabled for the calling process.</li>
</ul>
If the preceding conditions are not met, a call to this function does not fail, however, standard access policy is not enforced.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Client/Server Access Control Functions</a>



<a href="https://msdn.microsoft.com/8301ed4f-9458-410b-af19-4f055656005a">Client/Server Access Control Overview</a>



<a href="https://msdn.microsoft.com/5f4832b6-5cf5-4050-9e20-56674f2e2cb1">CreatePrivateObjectSecurity</a>



<a href="https://msdn.microsoft.com/4ef10852-8229-41de-a4d7-d2845e4c92ce">DestroyPrivateObjectSecurity</a>



<a href="https://msdn.microsoft.com/4043b76b-76b9-4111-8a29-a808b2412be0">GetFileSecurity</a>



<a href="https://msdn.microsoft.com/276e9657-5729-48cb-9531-14bfd08b7868">GetKernelObjectSecurity</a>



<a href="https://msdn.microsoft.com/998c2520-7833-4efd-a794-b13b528f0485">GetUserObjectSecurity</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a>



<a href="https://msdn.microsoft.com/726994c8-7813-4f1a-b7d7-a25e79202c33">SetPrivateObjectSecurity</a>
 

 

