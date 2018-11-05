---
UID: NF:securitybaseapi.SetSecurityDescriptorControl
title: SetSecurityDescriptorControl function
author: windows-sdk-content
description: Sets the control bits of a security descriptor. The function can set only the control bits that relate to automatic inheritance of ACEs.
old-location: security\setsecuritydescriptorcontrol.htm
tech.root: secauthz
ms.assetid: 672406af-ae04-4939-82a4-069a91e61b3f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: SetSecurityDescriptorControl, SetSecurityDescriptorControl function [Security], _win32_setsecuritydescriptorcontrol, security.setsecuritydescriptorcontrol, securitybaseapi/SetSecurityDescriptorControl
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
 - SetSecurityDescriptorControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetSecurityDescriptorControl function


## -description


The <b>SetSecurityDescriptorControl</b> function sets the control bits of a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a>. The function can set only the control bits that relate to automatic inheritance of ACEs. To set the other control bits of a security descriptor, use the functions, such as 
<a href="https://msdn.microsoft.com/a873b803-391e-47e1-af7e-6dad7195968c">SetSecurityDescriptorDacl</a>, for modifying the components of a security descriptor.


## -parameters




### -param pSecurityDescriptor [in]

A pointer to a 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure whose control and revision information are set.


### -param ControlBitsOfInterest [in]

A 
<a href="https://msdn.microsoft.com/9a4ef57e-c374-4ef6-99dc-1a8dd250f2c2">SECURITY_DESCRIPTOR_CONTROL</a> mask that indicates the control bits to set.


### -param ControlBitsToSet [in]

A 
<a href="https://msdn.microsoft.com/9a4ef57e-c374-4ef6-99dc-1a8dd250f2c2">SECURITY_DESCRIPTOR_CONTROL</a> mask that indicates the new values for the control bits specified by the <i>ControlBitsOfInterest</i> mask.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>SetSecurityDescriptorControl</b> function specifies the control bit or bits to modify, and whether the bits are on or off.


#### Examples

The following example marks the DACL on the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> as protected.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    SetSecurityDescriptorControl( &amp;SecDesc,
            SE_DACL_PROTECTED, SE_DACL_PROTECTED );
</pre>
</td>
</tr>
</table></span></div>
The following example marks the DACL as not protected.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    SetSecurityDescriptorControl( &amp;SecDesc,
            SE_DACL_PROTECTED, 0 );
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/d66682f2-8017-4245-9d93-5f8332a5b483">GetSecurityDescriptorControl</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/9a4ef57e-c374-4ef6-99dc-1a8dd250f2c2">SECURITY_DESCRIPTOR_CONTROL</a>



<a href="https://msdn.microsoft.com/a873b803-391e-47e1-af7e-6dad7195968c">SetSecurityDescriptorDacl</a>
 

 

