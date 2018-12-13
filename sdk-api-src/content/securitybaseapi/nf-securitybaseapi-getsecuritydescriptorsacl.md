---
UID: NF:securitybaseapi.GetSecurityDescriptorSacl
title: GetSecurityDescriptorSacl function
author: windows-sdk-content
description: Retrieves a pointer to the system access control list (SACL) in a specified security descriptor.
old-location: security\getsecuritydescriptorsacl.htm
tech.root: secauthz
ms.assetid: 6bf59735-aaa3-4751-8c98-00cc197df4e5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSecurityDescriptorSacl, GetSecurityDescriptorSacl function [Security], _win32_getsecuritydescriptorsacl, security.getsecuritydescriptorsacl, securitybaseapi/GetSecurityDescriptorSacl
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
 - GetSecurityDescriptorSacl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetSecurityDescriptorSacl function


## -description


The <b>GetSecurityDescriptorSacl</b> function retrieves a pointer to the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) in a specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a>.


## -parameters




### -param pSecurityDescriptor [in]

A pointer to the 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure that contains the SACL to which the function retrieves a pointer.


### -param lpbSaclPresent [out]

A pointer to a flag the function sets to indicate the presence of a SACL in the specified security descriptor. If this parameter is <b>TRUE</b>, the security descriptor contains a SACL, and the remaining output parameters in this function receive valid values. If this parameter is <b>FALSE</b>, the security descriptor does not contain a SACL, and the remaining output parameters do not receive valid values.


### -param pSacl [out]

A pointer to a pointer to an 
<a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL). If a SACL exists, the function sets the pointer pointed to by <i>pSacl</i> to the address of the security descriptor's SACL. If a SACL does not exist, no value is stored. 




If the function stores a <b>NULL</b> value in the pointer pointed to by <i>pSacl</i>, the security descriptor has a <b>NULL</b> SACL.


### -param lpbSaclDefaulted [out]

A pointer to a flag that is set to the value of the SE_SACL_DEFAULTED flag in the 
<a href="https://msdn.microsoft.com/9a4ef57e-c374-4ef6-99dc-1a8dd250f2c2">SECURITY_DESCRIPTOR_CONTROL</a> structure if a SACL exists for the security descriptor.


## -returns



If the function succeeds, the function returns nonzero.
      

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/d66682f2-8017-4245-9d93-5f8332a5b483">GetSecurityDescriptorControl</a>



<a href="https://msdn.microsoft.com/8006c8bb-4976-463f-b074-a59c3bbab36b">GetSecurityDescriptorDacl</a>



<a href="https://msdn.microsoft.com/a920b49e-a4c2-4e49-b529-88c12205d995">GetSecurityDescriptorGroup</a>



<a href="https://msdn.microsoft.com/eb331839-ff3e-4f4b-b93b-18da2ea72697">GetSecurityDescriptorLength</a>



<a href="https://msdn.microsoft.com/58e810db-348e-430c-a61f-79f67826b60d">GetSecurityDescriptorOwner</a>



<a href="https://msdn.microsoft.com/234fcda4-7d30-4c3f-a036-7ace58ca8a3c">InitializeSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/24a98229-11e4-45ef-988b-c2cf831275e7">IsValidSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="authorization_functions.htm">Low-level Access Control Functions</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/9a4ef57e-c374-4ef6-99dc-1a8dd250f2c2">SECURITY_DESCRIPTOR_CONTROL</a>



<a href="https://msdn.microsoft.com/21615b63-0619-4c0c-a1b8-88ed09a1235c">SetSecurityDescriptorSacl</a>
 

 

