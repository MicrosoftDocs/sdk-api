---
UID: NF:securitybaseapi.SetSecurityDescriptorRMControl
title: SetSecurityDescriptorRMControl function
author: windows-sdk-content
description: Sets the resource manager control bits in the SECURITY_DESCRIPTOR structure.
old-location: security\setsecuritydescriptorrmcontrol.htm
old-project: secauthz
ms.assetid: fe9c736b-e047-4aa3-a3de-d5f2f2cdab4f
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: SetSecurityDescriptorRMControl, SetSecurityDescriptorRMControl function [Security], _win32_setsecuritydescriptorrmcontrol, security.setsecuritydescriptorrmcontrol, securitybaseapi/SetSecurityDescriptorRMControl
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
 - SetSecurityDescriptorRMControl
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# SetSecurityDescriptorRMControl function


## -description


The <b>SetSecurityDescriptorRMControl</b> function sets the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager</a> control bits in the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure.


## -parameters




### -param SecurityDescriptor [in, out]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure that contains the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager</a> control bits.


### -param RMControl [in, optional]

A pointer to the bitfield value that the resource manager control bits in the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure will be set to. If the value of this parameter is <b>NULL</b>, the resource manager control bits will be cleared.


## -returns



The return value is ERROR_SUCCESS.




## -remarks



The resource manager control bits are eight bits in the <b>Sbz1</b> member of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a> structure that contains information specific to the resource manager accessing the structure. These bits should be accessed only through the 
<a href="https://msdn.microsoft.com/a1e2ce12-586b-4011-a82d-e246d5544367">GetSecurityDescriptorRMControl</a> and <b>SetSecurityDescriptorRMControl</b> functions.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/a1e2ce12-586b-4011-a82d-e246d5544367">GetSecurityDescriptorRMControl</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a>
 

 

