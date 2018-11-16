---
UID: NS:winnt._SECURITY_DESCRIPTOR
title: "_SECURITY_DESCRIPTOR"
author: windows-sdk-content
description: Contains the security information associated with an object.
old-location: security\security_descriptor.htm
tech.root: SecAuthZ
ms.assetid: 653992aa-4e32-4187-b3ac-727e82bfe0b6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PISECURITY_DESCRIPTOR, PISECURITY_DESCRIPTOR, PISECURITY_DESCRIPTOR structure pointer [Security], SECURITY_DESCRIPTOR, SECURITY_DESCRIPTOR structure [Security], _SECURITY_DESCRIPTOR, _win32_security_descriptor_str, security.security_descriptor, winnt/PISECURITY_DESCRIPTOR, winnt/SECURITY_DESCRIPTOR"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winnt.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - SECURITY_DESCRIPTOR
product: Windows
targetos: Windows
req.typenames: SECURITY_DESCRIPTOR, *PISECURITY_DESCRIPTOR
req.redist: 
---

# _SECURITY_DESCRIPTOR structure


## -description


The <b>SECURITY_DESCRIPTOR</b> structure contains the security information associated with an object. Applications use this structure to set and query an object's security status.

Because the internal format of a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> can vary, we recommend that applications  not modify the <b>SECURITY_DESCRIPTOR</b> structure directly. For creating and manipulating a security descriptor, use the functions listed in See Also.


## -struct-fields


## -remarks



A security descriptor includes information that specifies the following components of an object's security:

<ul>
<li>An owner <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID)</li>
<li>A primary group SID</li>
<li>A <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL)</li>
<li>A <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL)</li>
<li>Qualifiers for the preceding items</li>
</ul>
Several functions that use the <b>SECURITY_DESCRIPTOR</b> structure require that this structure be aligned on a valid pointer boundary in memory. These boundaries vary depending on the type of processor used. Memory allocation functions such as <b>malloc</b> and <b>LocalAlloc</b> return properly aligned pointers.




## -see-also




<a href="https://msdn.microsoft.com/d66682f2-8017-4245-9d93-5f8332a5b483">GetSecurityDescriptorControl</a>



<a href="https://msdn.microsoft.com/8006c8bb-4976-463f-b074-a59c3bbab36b">GetSecurityDescriptorDacl</a>



<a href="https://msdn.microsoft.com/a920b49e-a4c2-4e49-b529-88c12205d995">GetSecurityDescriptorGroup</a>



<a href="https://msdn.microsoft.com/eb331839-ff3e-4f4b-b93b-18da2ea72697">GetSecurityDescriptorLength</a>



<a href="https://msdn.microsoft.com/58e810db-348e-430c-a61f-79f67826b60d">GetSecurityDescriptorOwner</a>



<a href="https://msdn.microsoft.com/a1e2ce12-586b-4011-a82d-e246d5544367">GetSecurityDescriptorRMControl</a>



<a href="https://msdn.microsoft.com/6bf59735-aaa3-4751-8c98-00cc197df4e5">GetSecurityDescriptorSacl</a>



<a href="https://msdn.microsoft.com/234fcda4-7d30-4c3f-a036-7ace58ca8a3c">InitializeSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/24a98229-11e4-45ef-988b-c2cf831275e7">IsValidSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/a873b803-391e-47e1-af7e-6dad7195968c">SetSecurityDescriptorDacl</a>



<a href="https://msdn.microsoft.com/060c375c-a313-4fa2-8d85-cee9369c26a8">SetSecurityDescriptorGroup</a>



<a href="https://msdn.microsoft.com/cb3ba617-322a-4b8c-a9d5-32910315fb56">SetSecurityDescriptorOwner</a>



<a href="https://msdn.microsoft.com/fe9c736b-e047-4aa3-a3de-d5f2f2cdab4f">SetSecurityDescriptorRMControl</a>



<a href="https://msdn.microsoft.com/21615b63-0619-4c0c-a1b8-88ed09a1235c">SetSecurityDescriptorSacl</a>
 

 

