---
UID: NF:securitybaseapi.SetSecurityDescriptorDacl
title: SetSecurityDescriptorDacl function
author: windows-sdk-content
description: Sets information in a discretionary access control list (DACL). If a DACL is already present in the security descriptor, the DACL is replaced.
old-location: security\setsecuritydescriptordacl.htm
tech.root: secauthz
ms.assetid: a873b803-391e-47e1-af7e-6dad7195968c
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: SetSecurityDescriptorDacl, SetSecurityDescriptorDacl function [Security], _win32_setsecuritydescriptordacl, security.setsecuritydescriptordacl, securitybaseapi/SetSecurityDescriptorDacl
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
 - SetSecurityDescriptorDacl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetSecurityDescriptorDacl function


## -description


The <b>SetSecurityDescriptorDacl</b> function sets information in a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL). If a DACL is already present in the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a>, the DACL is replaced.


## -parameters




### -param pSecurityDescriptor [in, out]

A pointer to the 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure to which the function adds the DACL. This security descriptor must be in <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">absolute</a> format, meaning that its members must be pointers to other structures, rather than offsets to contiguous data.


### -param bDaclPresent [in]

A flag that indicates the presence of a DACL in the security descriptor. If this parameter is <b>TRUE</b>, the function sets the SE_DACL_PRESENT flag in the 
<a href="https://msdn.microsoft.com/9a4ef57e-c374-4ef6-99dc-1a8dd250f2c2">SECURITY_DESCRIPTOR_CONTROL</a> structure and uses the values in the <i>pDacl</i> and <i>bDaclDefaulted</i> parameters. If this parameter is <b>FALSE</b>, the function clears the SE_DACL_PRESENT flag, and <i>pDacl</i> and <i>bDaclDefaulted</i> are ignored.


### -param pDacl [in, optional]

A pointer to an 
<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a> structure that specifies the DACL for the security descriptor. If this parameter is <b>NULL</b>, a <b>NULL</b> DACL is assigned to the security descriptor, which allows all access to the object. The DACL is referenced by, not copied into, the security descriptor.


### -param bDaclDefaulted [in]

A flag that indicates the source of the DACL. If this flag is <b>TRUE</b>, the DACL has been retrieved by some default mechanism. If <b>FALSE</b>, the DACL has been explicitly specified by a user. The function stores this value in the SE_DACL_DEFAULTED flag of the <a href="https://msdn.microsoft.com/9a4ef57e-c374-4ef6-99dc-1a8dd250f2c2">SECURITY_DESCRIPTOR_CONTROL</a> structure. If this parameter is not specified, the SE_DACL_DEFAULTED flag is cleared.


## -returns



If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



There is an important difference between an empty and a nonexistent DACL. When a DACL is empty, it contains no <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs); therefore, no access rights are explicitly granted. As a result, access to the object is implicitly denied.

When an object has no DACL (when the <i>pDacl</i> parameter is <b>NULL</b>), no protection is assigned to the object, and all access requests are granted. To help maintain security, restrict access by using a DACL.

There are three possible outcomes in different configurations of the <i>bDaclPresent</i> flag and the <i>pDacl</i> parameter:

<ul>
<li>When the <i>pDacl</i> parameter points to a DACL and the <i>bDaclPresent</i> flag is <b>TRUE</b>, a DACL is specified and it must contain access-allowed ACEs to allow access to the object.</li>
<li>When the <i>pDacl</i> parameter does not point to a DACL and the <i>bDaclPresent</i> flag is <b>TRUE</b>, a <b>NULL</b> DACL is specified. All access is allowed. You should not use a <b>NULL</b> DACL with an object because any user can change the DACL and owner of the security descriptor. This will interfere with use of the object.</li>
<li>When the <i>pDacl</i> parameter does not point to a DACL and the <i>bDaclPresent</i> flag is <b>FALSE</b>, a DACL can be provided for the object through an inheritance or default mechanism.</li>
</ul>

#### Examples

For an example that uses this function, see <a href="https://msdn.microsoft.com/866992a7-95c4-4094-87bb-e6d8eeb24317">Creating a Security Descriptor for a New Object</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/8006c8bb-4976-463f-b074-a59c3bbab36b">GetSecurityDescriptorDacl</a>



<a href="https://msdn.microsoft.com/234fcda4-7d30-4c3f-a036-7ace58ca8a3c">InitializeSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/24a98229-11e4-45ef-988b-c2cf831275e7">IsValidSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="authorization_functions.htm">Low-level Access Control Functions</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/9a4ef57e-c374-4ef6-99dc-1a8dd250f2c2">SECURITY_DESCRIPTOR_CONTROL</a>



<a href="https://msdn.microsoft.com/060c375c-a313-4fa2-8d85-cee9369c26a8">SetSecurityDescriptorGroup</a>



<a href="https://msdn.microsoft.com/cb3ba617-322a-4b8c-a9d5-32910315fb56">SetSecurityDescriptorOwner</a>



<a href="https://msdn.microsoft.com/21615b63-0619-4c0c-a1b8-88ed09a1235c">SetSecurityDescriptorSacl</a>
 

 

