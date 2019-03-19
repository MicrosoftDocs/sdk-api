---
UID: NF:securitybaseapi.GetSecurityDescriptorDacl
title: GetSecurityDescriptorDacl function (securitybaseapi.h)
author: windows-sdk-content
description: Retrieves a pointer to the discretionary access control list (DACL) in a specified security descriptor.
old-location: security\getsecuritydescriptordacl.htm
tech.root: SecAuthZ
ms.assetid: 8006c8bb-4976-463f-b074-a59c3bbab36b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSecurityDescriptorDacl, GetSecurityDescriptorDacl function [Security], _win32_getsecuritydescriptordacl, security.getsecuritydescriptordacl, securitybaseapi/GetSecurityDescriptorDacl
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
 - GetSecurityDescriptorDacl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetSecurityDescriptorDacl function


## -description


The <b>GetSecurityDescriptorDacl</b> function retrieves a pointer to the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL) in a specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a>.


## -parameters




### -param pSecurityDescriptor [in]

A pointer to the 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure that contains the DACL. The function retrieves a pointer to it.


### -param lpbDaclPresent [out]

A pointer to a value that indicates the presence of a DACL in the specified security descriptor. If <i>lpbDaclPresent</i> is <b>TRUE</b>, the security descriptor contains a DACL, and the remaining output parameters in this function receive valid values. If <i>lpbDaclPresent</i> is <b>FALSE</b>, the security descriptor does not contain a DACL, and the remaining output parameters do not receive valid values.

A value of <b>TRUE</b> for <i>lpbDaclPresent</i> does not mean that <i>pDacl</i> is not <b>NULL</b>.  That is, <i>lpbDaclPresent</i> can be <b>TRUE</b> while <i>pDacl</i> is <b>NULL</b>, meaning that a <b>NULL</b> DACL is in effect.   A <b>NULL</b> DACL implicitly allows all access to an object and is not the same as an empty DACL. An empty DACL permits no access to an object.  For information about creating a proper DACL, see <a href="https://msdn.microsoft.com/f8ec202f-4f34-4123-8f3c-cfc5960b4dc2">Creating a DACL</a>.


### -param pDacl [out]

A pointer to a pointer to an 
<a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL). If a DACL exists, the function sets the pointer pointed to by <i>pDacl</i> to the address of the security descriptor's DACL. If a DACL does not exist, no value is stored. 




If the function stores a <b>NULL</b> value in the pointer pointed to by <i>pDacl</i>, the security descriptor has a <b>NULL</b> DACL. A <b>NULL</b> DACL implicitly allows all access to an object.

If an application expects a non-<b>NULL</b> DACL but encounters a <b>NULL</b> DACL, the application should fail securely and not allow access. 


### -param lpbDaclDefaulted [out]

A pointer to a flag set to the value of the SE_DACL_DEFAULTED flag in the 
<a href="https://msdn.microsoft.com/9a4ef57e-c374-4ef6-99dc-1a8dd250f2c2">SECURITY_DESCRIPTOR_CONTROL</a> structure if a DACL exists for the security descriptor. If this flag is <b>TRUE</b>, the DACL was retrieved by a default mechanism; if <b>FALSE</b>, the DACL was explicitly specified by a user.


## -returns



If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/d66682f2-8017-4245-9d93-5f8332a5b483">GetSecurityDescriptorControl</a>



<a href="https://msdn.microsoft.com/a920b49e-a4c2-4e49-b529-88c12205d995">GetSecurityDescriptorGroup</a>



<a href="https://msdn.microsoft.com/eb331839-ff3e-4f4b-b93b-18da2ea72697">GetSecurityDescriptorLength</a>



<a href="https://msdn.microsoft.com/58e810db-348e-430c-a61f-79f67826b60d">GetSecurityDescriptorOwner</a>



<a href="https://msdn.microsoft.com/6bf59735-aaa3-4751-8c98-00cc197df4e5">GetSecurityDescriptorSacl</a>



<a href="https://msdn.microsoft.com/234fcda4-7d30-4c3f-a036-7ace58ca8a3c">InitializeSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/24a98229-11e4-45ef-988b-c2cf831275e7">IsValidSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Low-level Access Control Functions</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/9a4ef57e-c374-4ef6-99dc-1a8dd250f2c2">SECURITY_DESCRIPTOR_CONTROL</a>



<a href="https://msdn.microsoft.com/a873b803-391e-47e1-af7e-6dad7195968c">SetSecurityDescriptorDacl</a>
 

 

