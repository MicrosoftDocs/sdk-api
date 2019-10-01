---
UID: NF:securitybaseapi.InitializeSecurityDescriptor
title: InitializeSecurityDescriptor function (securitybaseapi.h)
author: windows-sdk-content
description: Initializes a new security descriptor.
old-location: security\initializesecuritydescriptor.htm
tech.root: SecAuthZ
ms.assetid: 234fcda4-7d30-4c3f-a036-7ace58ca8a3c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InitializeSecurityDescriptor, InitializeSecurityDescriptor function [Security], _win32_initializesecuritydescriptor, security.initializesecuritydescriptor, securitybaseapi/InitializeSecurityDescriptor
ms.topic: function
f1_keywords:
- securitybaseapi/InitializeSecurityDescriptor
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
- InitializeSecurityDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InitializeSecurityDescriptor function


## -description


The <b>InitializeSecurityDescriptor</b> function initializes a new <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security descriptor</a>.


## -parameters




### -param pSecurityDescriptor [out]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure that the function initializes.


### -param dwRevision [in]

The revision level to assign to the security descriptor. This parameter must be SECURITY_DESCRIPTOR_REVISION.


## -returns



If the function succeeds, the function returns nonzero.
      

If the function fails, it returns zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The <b>InitializeSecurityDescriptor</b> function initializes a security descriptor in <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">absolute</a> format, rather than <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">self-relative</a> format.

The <b>InitializeSecurityDescriptor</b> function initializes a security descriptor to have no <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL), no <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL), no owner, no primary group, and all control flags set to <b>FALSE</b> (<b>NULL</b>). Thus, except for its revision level, it is empty.


#### Examples

For an example that uses this function, see <a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--">Creating a Security Descriptor for a New Object</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol">GetSecurityDescriptorControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl">GetSecurityDescriptorDacl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup">GetSecurityDescriptorGroup</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorlength">GetSecurityDescriptorLength</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner">GetSecurityDescriptorOwner</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl">GetSecurityDescriptorSacl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsecuritydescriptor">IsValidSecurityDescriptor</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl">SetSecurityDescriptorDacl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup">SetSecurityDescriptorGroup</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner">SetSecurityDescriptorOwner</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl">SetSecurityDescriptorSacl</a>
 

 

