---
UID: NF:securitybaseapi.SetSecurityDescriptorControl
title: SetSecurityDescriptorControl function (securitybaseapi.h)
description: Sets the control bits of a security descriptor. The function can set only the control bits that relate to automatic inheritance of ACEs.
helpviewer_keywords: ["SetSecurityDescriptorControl","SetSecurityDescriptorControl function [Security]","_win32_setsecuritydescriptorcontrol","security.setsecuritydescriptorcontrol","securitybaseapi/SetSecurityDescriptorControl"]
old-location: security\setsecuritydescriptorcontrol.htm
tech.root: security
ms.assetid: 672406af-ae04-4939-82a4-069a91e61b3f
ms.date: 12/05/2018
ms.keywords: SetSecurityDescriptorControl, SetSecurityDescriptorControl function [Security], _win32_setsecuritydescriptorcontrol, security.setsecuritydescriptorcontrol, securitybaseapi/SetSecurityDescriptorControl
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
 - SetSecurityDescriptorControl
 - securitybaseapi/SetSecurityDescriptorControl
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
 - SetSecurityDescriptorControl
---

# SetSecurityDescriptorControl function


## -description

The <b>SetSecurityDescriptorControl</b> function sets the control bits of a <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a>. The function can set only the control bits that relate to automatic inheritance of ACEs. To set the other control bits of a security descriptor, use the functions, such as 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl">SetSecurityDescriptorDacl</a>, for modifying the components of a security descriptor.

## -parameters

### -param pSecurityDescriptor [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure whose control and revision information are set.

### -param ControlBitsOfInterest [in]

A 
<a href="/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a> mask that indicates the control bits to set.

### -param ControlBitsToSet [in]

A 
<a href="/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a> mask that indicates the new values for the control bits specified by the <i>ControlBitsOfInterest</i> mask.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>SetSecurityDescriptorControl</b> function specifies the control bit or bits to modify, and whether the bits are on or off.


#### Examples

The following example marks the DACL on the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> as protected.


```cpp
    SetSecurityDescriptorControl( &SecDesc,
            SE_DACL_PROTECTED, SE_DACL_PROTECTED );

```


The following example marks the DACL as not protected.


```cpp
    SetSecurityDescriptorControl( &SecDesc,
            SE_DACL_PROTECTED, 0 );

```

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol">GetSecurityDescriptorControl</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl">SetSecurityDescriptorDacl</a>