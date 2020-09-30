---
UID: NS:winnt._SECURITY_DESCRIPTOR
title: SECURITY_DESCRIPTOR (winnt.h)
description: Contains the security information associated with an object.
helpviewer_keywords: ["*PISECURITY_DESCRIPTOR","PISECURITY_DESCRIPTOR","PISECURITY_DESCRIPTOR structure pointer [Security]","SECURITY_DESCRIPTOR","SECURITY_DESCRIPTOR structure [Security]","_SECURITY_DESCRIPTOR","_win32_security_descriptor_str","security.security_descriptor","winnt/PISECURITY_DESCRIPTOR","winnt/SECURITY_DESCRIPTOR"]
old-location: security\security_descriptor.htm
tech.root: security
ms.assetid: 653992aa-4e32-4187-b3ac-727e82bfe0b6
ms.date: 12/05/2018
ms.keywords: '*PISECURITY_DESCRIPTOR, PISECURITY_DESCRIPTOR, PISECURITY_DESCRIPTOR structure pointer [Security], SECURITY_DESCRIPTOR, SECURITY_DESCRIPTOR structure [Security], _SECURITY_DESCRIPTOR, _win32_security_descriptor_str, security.security_descriptor, winnt/PISECURITY_DESCRIPTOR, winnt/SECURITY_DESCRIPTOR'
req.header: winnt.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SECURITY_DESCRIPTOR, *PISECURITY_DESCRIPTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECURITY_DESCRIPTOR
 - winnt/_SECURITY_DESCRIPTOR
 - PISECURITY_DESCRIPTOR
 - winnt/PISECURITY_DESCRIPTOR
 - SECURITY_DESCRIPTOR
 - winnt/SECURITY_DESCRIPTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - SECURITY_DESCRIPTOR
---

# SECURITY_DESCRIPTOR structure


## -description

The <b>SECURITY_DESCRIPTOR</b> structure contains the security information associated with an object. Applications use this structure to set and query an object's security status.

Because the internal format of a <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> can vary, we recommend that applications  not modify the <b>SECURITY_DESCRIPTOR</b> structure directly. For creating and manipulating a security descriptor, use the functions listed in See Also.

## -struct-fields

## -remarks

A security descriptor includes information that specifies the following components of an object's security:

<ul>
<li>An owner <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID)</li>
<li>A primary group SID</li>
<li>A <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL)</li>
<li>A <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL)</li>
<li>Qualifiers for the preceding items</li>
</ul>
Several functions that use the <b>SECURITY_DESCRIPTOR</b> structure require that this structure be aligned on a valid pointer boundary in memory. These boundaries vary depending on the type of processor used. Memory allocation functions such as <b>malloc</b> and <b>LocalAlloc</b> return properly aligned pointers.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol">GetSecurityDescriptorControl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl">GetSecurityDescriptorDacl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup">GetSecurityDescriptorGroup</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorlength">GetSecurityDescriptorLength</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner">GetSecurityDescriptorOwner</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorrmcontrol">GetSecurityDescriptorRMControl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl">GetSecurityDescriptorSacl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor">InitializeSecurityDescriptor</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsecuritydescriptor">IsValidSecurityDescriptor</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl">SetSecurityDescriptorDacl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup">SetSecurityDescriptorGroup</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner">SetSecurityDescriptorOwner</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorrmcontrol">SetSecurityDescriptorRMControl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl">SetSecurityDescriptorSacl</a>