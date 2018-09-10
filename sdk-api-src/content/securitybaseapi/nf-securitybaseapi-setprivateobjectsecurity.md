---
UID: NF:securitybaseapi.SetPrivateObjectSecurity
title: SetPrivateObjectSecurity function
author: windows-sdk-content
description: Modifies a private object's security descriptor.
old-location: security\setprivateobjectsecurity.htm
tech.root: SecAuthZ
ms.assetid: 726994c8-7813-4f1a-b7d7-a25e79202c33
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SetPrivateObjectSecurity, SetPrivateObjectSecurity function [Security], _win32_setprivateobjectsecurity, security.setprivateobjectsecurity, securitybaseapi/SetPrivateObjectSecurity
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - SetPrivateObjectSecurity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetPrivateObjectSecurity function


## -description


The <b>SetPrivateObjectSecurity</b> function modifies a private object's <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a>.

To specify whether the protected server supports automatic inheritance of <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs), use the 
<a href="https://msdn.microsoft.com/eb3a751f-741e-448f-b812-5f16a4040b5e">SetPrivateObjectSecurityEx</a> function.


## -parameters




### -param SecurityInformation [in]

Indicates the parts of the security descriptor to set. This value can be a combination of the 
<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a> bit flags.


### -param ModificationDescriptor [in]

A pointer to a 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure. The parts of this security descriptor indicated by the <i>SecurityInformation</i> parameter are applied to the <i>ObjectsSecurityDescriptor</i> security descriptor.


### -param ObjectsSecurityDescriptor [in, out]

A pointer to a pointer to a <a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure. This security descriptor must be in <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">self-relative</a> form. 




On input, this is the current security descriptor of the private object. The function modifies it to produce the new security descriptor. If necessary, the <b>SetPrivateObjectSecurity</b> function allocates additional memory to produce a larger security descriptor.


### -param GenericMapping [in]

A pointer to a 
<a href="https://msdn.microsoft.com/e3c49b47-9bc7-4000-a131-449345ebb9cd">GENERIC_MAPPING</a> structure that specifies the specific and standard access rights that correspond to each of the generic access rights.


### -param Token [in, optional]

A handle to the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a> for the client on whose behalf the private object's security is being modified. This parameter is required to ensure that the client has provided a legitimate value for a new owner <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID). The token must be open for TOKEN_QUERY access.


## -returns



If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function is intended for use by resource managers only. To implement the standard access control semantics for updating security descriptors, a resource manager should verify that the following conditions are met before calling <b>SetPrivateObjectSecurity</b>:

<ul>
<li>If the object's owner is being set, the calling <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a> must have either WRITE_OWNER permission or be the object's owner.</li>
<li>If the object's <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL) is being set, the calling process must have either WRITE_DAC permission or be the object's owner.</li>
<li>If the object's <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) is being set, the SE_SECURITY_NAME privilege must be enabled for the calling process.</li>
</ul>
If the preceding conditions are not met, a call to this function does not fail; however, standard access policy is not enforced.

The process calling this function should not be impersonating a client because clients do not typically have appropriate privileges required for underlying token operations.




## -see-also




<a href="authorization_functions.htm">Client/Server Access Control Functions</a>



<a href="https://msdn.microsoft.com/8301ed4f-9458-410b-af19-4f055656005a">Client/Server Access Control Overview</a>



<a href="https://msdn.microsoft.com/5f4832b6-5cf5-4050-9e20-56674f2e2cb1">CreatePrivateObjectSecurity</a>



<a href="https://msdn.microsoft.com/4ef10852-8229-41de-a4d7-d2845e4c92ce">DestroyPrivateObjectSecurity</a>



<a href="https://msdn.microsoft.com/e3c49b47-9bc7-4000-a131-449345ebb9cd">GENERIC_MAPPING</a>



<a href="https://msdn.microsoft.com/3e93c0a0-e449-4df1-812b-c3fb0dfe9c19">GetPrivateObjectSecurity</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a>



<a href="https://msdn.microsoft.com/27766c97-7ac5-40fc-b798-7cd07e496c0d">SetFileSecurity</a>



<a href="https://msdn.microsoft.com/2a70483e-245d-4bc7-b90a-58d143364ce1">SetKernelObjectSecurity</a>



<a href="https://msdn.microsoft.com/eb3a751f-741e-448f-b812-5f16a4040b5e">SetPrivateObjectSecurityEx</a>



<a href="https://msdn.microsoft.com/219e41b8-9ac7-4747-a585-b6b9df6a1c9c">SetUserObjectSecurity</a>
 

 

