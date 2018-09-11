---
UID: NF:securitybaseapi.IsValidSecurityDescriptor
title: IsValidSecurityDescriptor function
author: windows-sdk-content
description: Determines whether the components of a security descriptor are valid.
old-location: security\isvalidsecuritydescriptor.htm
tech.root: SecAuthZ
ms.assetid: 24a98229-11e4-45ef-988b-c2cf831275e7
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IsValidSecurityDescriptor, IsValidSecurityDescriptor function [Security], _win32_isvalidsecuritydescriptor, security.isvalidsecuritydescriptor, securitybaseapi/IsValidSecurityDescriptor
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
 - IsValidSecurityDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsValidSecurityDescriptor function


## -description


The <b>IsValidSecurityDescriptor</b> function determines whether the components of a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> are valid.


## -parameters




### -param pSecurityDescriptor [in]

A pointer to a 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure that the function validates.


## -returns



If the components of the security descriptor are valid, the return value is nonzero.

If any of the components of the security descriptor are not valid, the return value is zero. There is no extended error information for this function; do not call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>IsValidSecurityDescriptor</b> function checks the validity of the components that are present in the security descriptor. It does not verify whether certain components are present nor does it verify the contents of the individual ACE or ACL.




## -see-also




<a href="https://msdn.microsoft.com/d66682f2-8017-4245-9d93-5f8332a5b483">GetSecurityDescriptorControl</a>



<a href="https://msdn.microsoft.com/8006c8bb-4976-463f-b074-a59c3bbab36b">GetSecurityDescriptorDacl</a>



<a href="https://msdn.microsoft.com/a920b49e-a4c2-4e49-b529-88c12205d995">GetSecurityDescriptorGroup</a>



<a href="https://msdn.microsoft.com/eb331839-ff3e-4f4b-b93b-18da2ea72697">GetSecurityDescriptorLength</a>



<a href="https://msdn.microsoft.com/58e810db-348e-430c-a61f-79f67826b60d">GetSecurityDescriptorOwner</a>



<a href="https://msdn.microsoft.com/6bf59735-aaa3-4751-8c98-00cc197df4e5">GetSecurityDescriptorSacl</a>



<a href="https://msdn.microsoft.com/234fcda4-7d30-4c3f-a036-7ace58ca8a3c">InitializeSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/3ae9f147-4e90-44df-a1af-cf6ebad92aea">IsValidAcl</a>



<a href="https://msdn.microsoft.com/0fb08512-90a1-4a5c-9b4c-121bf7701bba">IsValidSid</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Low-level Access Control Functions</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/a873b803-391e-47e1-af7e-6dad7195968c">SetSecurityDescriptorDacl</a>



<a href="https://msdn.microsoft.com/060c375c-a313-4fa2-8d85-cee9369c26a8">SetSecurityDescriptorGroup</a>



<a href="https://msdn.microsoft.com/cb3ba617-322a-4b8c-a9d5-32910315fb56">SetSecurityDescriptorOwner</a>



<a href="https://msdn.microsoft.com/21615b63-0619-4c0c-a1b8-88ed09a1235c">SetSecurityDescriptorSacl</a>
 

 

