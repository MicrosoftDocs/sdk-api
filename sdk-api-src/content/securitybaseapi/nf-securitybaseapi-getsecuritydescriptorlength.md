---
UID: NF:securitybaseapi.GetSecurityDescriptorLength
title: GetSecurityDescriptorLength function (securitybaseapi.h)
author: windows-sdk-content
description: Returns the length, in bytes, of a structurally valid security descriptor. The length includes the length of all associated structures.
old-location: security\getsecuritydescriptorlength.htm
tech.root: SecAuthZ
ms.assetid: eb331839-ff3e-4f4b-b93b-18da2ea72697
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSecurityDescriptorLength, GetSecurityDescriptorLength function [Security], _win32_getsecuritydescriptorlength, security.getsecuritydescriptorlength, securitybaseapi/GetSecurityDescriptorLength
ms.topic: function
f1_keywords: ["securitybaseapi/GetSecurityDescriptorLength"]
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
 - GetSecurityDescriptorLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetSecurityDescriptorLength function


## -description


The <b>GetSecurityDescriptorLength</b> function returns the length, in bytes, of a structurally valid <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security descriptor</a>. The length includes the length of all associated structures.


## -parameters




### -param pSecurityDescriptor [in]

A pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_security_descriptor">SECURITY_DESCRIPTOR</a> structure whose length the function returns. The pointer is assumed to be valid.


## -returns



If the function succeeds, the function returns the length, in bytes, of the <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_security_descriptor">SECURITY_DESCRIPTOR</a> structure.

If the <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_security_descriptor">SECURITY_DESCRIPTOR</a> structure is not valid, the return value is undefined.




## -remarks



The minimum length of a security descriptor is SECURITY_DESCRIPTOR_MIN_LENGTH. A security descriptor of this length has no associated 
<a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs) or 
<a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">access control lists</a> (ACLs).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol">GetSecurityDescriptorControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl">GetSecurityDescriptorDacl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup">GetSecurityDescriptorGroup</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner">GetSecurityDescriptorOwner</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl">GetSecurityDescriptorSacl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsecuritydescriptor">IsValidSecurityDescriptor</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_security_descriptor">SECURITY_DESCRIPTOR</a>
 

 

