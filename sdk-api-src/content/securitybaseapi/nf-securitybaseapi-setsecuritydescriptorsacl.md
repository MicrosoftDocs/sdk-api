---
UID: NF:securitybaseapi.SetSecurityDescriptorSacl
title: SetSecurityDescriptorSacl function
author: windows-sdk-content
description: Sets information in a system access control list (SACL). If there is already a SACL present in the security descriptor, it is replaced.
old-location: security\setsecuritydescriptorsacl.htm
tech.root: secauthz
ms.assetid: 21615b63-0619-4c0c-a1b8-88ed09a1235c
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: SetSecurityDescriptorSacl, SetSecurityDescriptorSacl function [Security], _win32_setsecuritydescriptorsacl, security.setsecuritydescriptorsacl, securitybaseapi/SetSecurityDescriptorSacl
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
 - SetSecurityDescriptorSacl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetSecurityDescriptorSacl function


## -description


The <b>SetSecurityDescriptorSacl</b> function sets information in a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL). If there is already a SACL present in the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a>, it is replaced.


## -parameters




### -param pSecurityDescriptor [in, out]

A pointer to the 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure to which the function adds the SACL. This security descriptor must be in absolute format, meaning that its members must be pointers to other structures, rather than offsets to contiguous data.


### -param bSaclPresent [in]

Indicates the presence of a SACL in the security descriptor. If this parameter is <b>TRUE</b>, the function sets the SE_SACL_PRESENT flag in the 
<a href="https://msdn.microsoft.com/9a4ef57e-c374-4ef6-99dc-1a8dd250f2c2">SECURITY_DESCRIPTOR_CONTROL</a> structure and uses the values in the <i>pSacl</i> and <i>bSaclDefaulted</i> parameters. If it is <b>FALSE</b>, the function does not set the SE_SACL_PRESENT flag, and <i>pSacl</i> and <i>bSaclDefaulted</i> are ignored.


### -param pSacl [in, optional]

A pointer to an 
<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a> structure that specifies the SACL for the security descriptor. If this parameter is <b>NULL</b>, a <b>NULL</b> SACL is assigned to the security descriptor. The SACL is referenced by, not copied into, the security descriptor.


### -param bSaclDefaulted [in]

Indicates the source of the SACL. If this flag is <b>TRUE</b>, the SACL has been retrieved by some default mechanism. If it is <b>FALSE</b>, the SACL has been explicitly specified by a user. The function stores this value in the SE_SACL_DEFAULTED flag of the <a href="https://msdn.microsoft.com/9a4ef57e-c374-4ef6-99dc-1a8dd250f2c2">SECURITY_DESCRIPTOR_CONTROL</a> structure. If this parameter is not specified, the SE_SACL_DEFAULTED flag is cleared.


## -returns



If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a>



<a href="https://msdn.microsoft.com/6bf59735-aaa3-4751-8c98-00cc197df4e5">GetSecurityDescriptorSacl</a>



<a href="https://msdn.microsoft.com/234fcda4-7d30-4c3f-a036-7ace58ca8a3c">InitializeSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/24a98229-11e4-45ef-988b-c2cf831275e7">IsValidSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="authorization_functions.htm">Low-level Access Control Functions</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/9a4ef57e-c374-4ef6-99dc-1a8dd250f2c2">SECURITY_DESCRIPTOR_CONTROL</a>



<a href="https://msdn.microsoft.com/a873b803-391e-47e1-af7e-6dad7195968c">SetSecurityDescriptorDacl</a>



<a href="https://msdn.microsoft.com/060c375c-a313-4fa2-8d85-cee9369c26a8">SetSecurityDescriptorGroup</a>



<a href="https://msdn.microsoft.com/cb3ba617-322a-4b8c-a9d5-32910315fb56">SetSecurityDescriptorOwner</a>
 

 

