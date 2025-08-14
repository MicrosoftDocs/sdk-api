---
UID: NF:securitybaseapi.GetSecurityDescriptorControl
title: GetSecurityDescriptorControl function (securitybaseapi.h)
description: Retrieves a security descriptor control and revision information.
helpviewer_keywords: ["GetSecurityDescriptorControl","GetSecurityDescriptorControl function [Security]","_win32_getsecuritydescriptorcontrol","security.getsecuritydescriptorcontrol","securitybaseapi/GetSecurityDescriptorControl"]
old-location: security\getsecuritydescriptorcontrol.htm
tech.root: security
ms.assetid: d66682f2-8017-4245-9d93-5f8332a5b483
ms.date: 12/05/2018
ms.keywords: GetSecurityDescriptorControl, GetSecurityDescriptorControl function [Security], _win32_getsecuritydescriptorcontrol, security.getsecuritydescriptorcontrol, securitybaseapi/GetSecurityDescriptorControl
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
 - GetSecurityDescriptorControl
 - securitybaseapi/GetSecurityDescriptorControl
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
 - GetSecurityDescriptorControl
---

# GetSecurityDescriptorControl function


## -description

The <b>GetSecurityDescriptorControl</b> function retrieves a <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> control and revision information.

## -parameters

### -param pSecurityDescriptor [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure whose control and revision information the function retrieves.

### -param pControl [out]

A pointer to a 
<a href="/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a> structure that receives the security descriptor's control information.

### -param lpdwRevision [out]

A pointer to a variable that receives the security descriptor's revision value. This value is always set, even when <b>GetSecurityDescriptorControl</b> returns an error.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl">GetSecurityDescriptorDacl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup">GetSecurityDescriptorGroup</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorlength">GetSecurityDescriptorLength</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner">GetSecurityDescriptorOwner</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl">GetSecurityDescriptorSacl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsecuritydescriptor">IsValidSecurityDescriptor</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a>