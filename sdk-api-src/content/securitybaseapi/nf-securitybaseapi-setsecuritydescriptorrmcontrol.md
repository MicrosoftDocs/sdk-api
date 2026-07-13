---
UID: NF:securitybaseapi.SetSecurityDescriptorRMControl
title: SetSecurityDescriptorRMControl function (securitybaseapi.h)
description: Sets the resource manager control bits in the SECURITY_DESCRIPTOR structure.
helpviewer_keywords: ["SetSecurityDescriptorRMControl","SetSecurityDescriptorRMControl function [Security]","_win32_setsecuritydescriptorrmcontrol","security.setsecuritydescriptorrmcontrol","securitybaseapi/SetSecurityDescriptorRMControl"]
old-location: security\setsecuritydescriptorrmcontrol.htm
tech.root: security
ms.assetid: fe9c736b-e047-4aa3-a3de-d5f2f2cdab4f
ms.date: 12/05/2018
ms.keywords: SetSecurityDescriptorRMControl, SetSecurityDescriptorRMControl function [Security], _win32_setsecuritydescriptorrmcontrol, security.setsecuritydescriptorrmcontrol, securitybaseapi/SetSecurityDescriptorRMControl
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetSecurityDescriptorRMControl
 - securitybaseapi/SetSecurityDescriptorRMControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
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
---

# SetSecurityDescriptorRMControl function


## -description

The <b>SetSecurityDescriptorRMControl</b> function sets the <a href="/windows/desktop/SecGloss/r-gly">resource manager</a> control bits in the 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure.

## -parameters

### -param SecurityDescriptor [in, out]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure that contains the <a href="/windows/desktop/SecGloss/r-gly">resource manager</a> control bits.

### -param RMControl [in, optional]

A pointer to the bitfield value that the resource manager control bits in the 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure will be set to. If the value of this parameter is <b>NULL</b>, the resource manager control bits will be cleared.

## -returns

The return value is ERROR_SUCCESS.

## -remarks

The resource manager control bits are eight bits in the <b>Sbz1</b> member of the 
<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> structure that contains information specific to the resource manager accessing the structure. These bits should be accessed only through the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorrmcontrol">GetSecurityDescriptorRMControl</a> and <b>SetSecurityDescriptorRMControl</b> functions.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorrmcontrol">GetSecurityDescriptorRMControl</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>