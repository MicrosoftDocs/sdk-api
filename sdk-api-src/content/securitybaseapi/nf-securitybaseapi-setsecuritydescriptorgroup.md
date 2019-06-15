---
UID: NF:securitybaseapi.SetSecurityDescriptorGroup
title: SetSecurityDescriptorGroup function (securitybaseapi.h)
author: windows-sdk-content
description: Sets the primary group information of an absolute-format security descriptor, replacing any primary group information already present in the security descriptor.
old-location: security\setsecuritydescriptorgroup.htm
tech.root: SecAuthZ
ms.assetid: 060c375c-a313-4fa2-8d85-cee9369c26a8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetSecurityDescriptorGroup, SetSecurityDescriptorGroup function [Security], _win32_setsecuritydescriptorgroup, security.setsecuritydescriptorgroup, securitybaseapi/SetSecurityDescriptorGroup
ms.topic: function
f1_keywords: ["securitybaseapi/SetSecurityDescriptorGroup"]
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
 - SetSecurityDescriptorGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetSecurityDescriptorGroup function


## -description


The <b>SetSecurityDescriptorGroup</b> function sets the primary group information of an absolute-format <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security descriptor</a>, replacing any primary group information already present in the security descriptor.


## -parameters




### -param pSecurityDescriptor [in, out]

A pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_security_descriptor">SECURITY_DESCRIPTOR</a> structure whose primary group is set by this function. The function replaces any existing primary group with the new primary group.


### -param pGroup [in, optional]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_sid">SID</a> structure for the security descriptor's new primary group. The <b>SID</b> structure is referenced by, not copied into, the security descriptor. If this parameter is <b>NULL</b>, the function clears the security descriptor's primary group information. This marks the security descriptor as having no primary group.


### -param bGroupDefaulted [in]

Indicates whether the primary group information was derived from a default mechanism. If this value is <b>TRUE</b>, it is default information, and the function stores this value as the SE_GROUP_DEFAULTED flag in the 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a> structure. If this parameter is zero, the SE_GROUP_DEFAULTED flag is cleared.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup">GetSecurityDescriptorGroup</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor">InitializeSecurityDescriptor</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_sid">SID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl">SetSecurityDescriptorDacl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner">SetSecurityDescriptorOwner</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl">SetSecurityDescriptorSacl</a>
 

 

