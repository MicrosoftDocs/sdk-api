---
UID: NF:securitybaseapi.SetSecurityDescriptorOwner
title: SetSecurityDescriptorOwner function
author: windows-sdk-content
description: Sets the owner information of an absolute-format security descriptor. It replaces any owner information already present in the security descriptor.
old-location: security\setsecuritydescriptorowner.htm
old-project: SecAuthZ
ms.assetid: cb3ba617-322a-4b8c-a9d5-32910315fb56
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: SetSecurityDescriptorOwner, SetSecurityDescriptorOwner function [Security], _win32_setsecuritydescriptorowner, security.setsecuritydescriptorowner, securitybaseapi/SetSecurityDescriptorOwner
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: EXTENDED_NAME_FORMAT, *PEXTENDED_NAME_FORMAT
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
 - SetSecurityDescriptorOwner
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# SetSecurityDescriptorOwner function


## -description


The <b>SetSecurityDescriptorOwner</b> function sets the owner information of an absolute-format <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a>. It replaces any owner information already present in the security descriptor.


## -parameters




### -param pSecurityDescriptor [in, out]

A pointer to the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure whose owner is set by this function. The function replaces any existing owner with the new owner.


### -param pOwner [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure for the security descriptor's new primary owner. The <b>SID</b> structure is referenced by, not copied into, the security descriptor. If this parameter is <b>NULL</b>, the function clears the security descriptor's owner information. This marks the security descriptor as having no owner.


### -param bOwnerDefaulted [in]

Indicates whether the owner information is derived from a default mechanism. If this value is <b>TRUE</b>, it is default information. The function stores this value as the SE_OWNER_DEFAULTED flag in the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556619">SECURITY_DESCRIPTOR_CONTROL</a> structure. If this parameter is zero, the SE_OWNER_DEFAULTED flag is cleared.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/58e810db-348e-430c-a61f-79f67826b60d">GetSecurityDescriptorOwner</a>



<a href="https://msdn.microsoft.com/234fcda4-7d30-4c3f-a036-7ace58ca8a3c">InitializeSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/24a98229-11e4-45ef-988b-c2cf831275e7">IsValidSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="authorization_functions.htm">Low-level Access Control Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556619">SECURITY_DESCRIPTOR_CONTROL</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>



<a href="https://msdn.microsoft.com/a873b803-391e-47e1-af7e-6dad7195968c">SetSecurityDescriptorDacl</a>



<a href="https://msdn.microsoft.com/060c375c-a313-4fa2-8d85-cee9369c26a8">SetSecurityDescriptorGroup</a>



<a href="https://msdn.microsoft.com/21615b63-0619-4c0c-a1b8-88ed09a1235c">SetSecurityDescriptorSacl</a>
 

 

