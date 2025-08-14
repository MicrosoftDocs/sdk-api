---
UID: NF:securitybaseapi.SetPrivateObjectSecurity
title: SetPrivateObjectSecurity function (securitybaseapi.h)
description: Modifies a private object's security descriptor.
helpviewer_keywords: ["SetPrivateObjectSecurity","SetPrivateObjectSecurity function [Security]","_win32_setprivateobjectsecurity","security.setprivateobjectsecurity","securitybaseapi/SetPrivateObjectSecurity"]
old-location: security\setprivateobjectsecurity.htm
tech.root: security
ms.assetid: 726994c8-7813-4f1a-b7d7-a25e79202c33
ms.date: 12/05/2018
ms.keywords: SetPrivateObjectSecurity, SetPrivateObjectSecurity function [Security], _win32_setprivateobjectsecurity, security.setprivateobjectsecurity, securitybaseapi/SetPrivateObjectSecurity
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - SetPrivateObjectSecurity
 - securitybaseapi/SetPrivateObjectSecurity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - api-ms-win-downlevel-advapi32-l1-1-0.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - SetPrivateObjectSecurity
---

# SetPrivateObjectSecurity function


## -description

The <b>SetPrivateObjectSecurity</b> function modifies a private object's <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a>.

To specify whether the protected server supports automatic inheritance of <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs), use the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurityex">SetPrivateObjectSecurityEx</a> function.

## -parameters

### -param SecurityInformation [in]

Indicates the parts of the security descriptor to set. This value can be a combination of the 
<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> bit flags.

### -param ModificationDescriptor [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure. The parts of this security descriptor indicated by the <i>SecurityInformation</i> parameter are applied to the <i>ObjectsSecurityDescriptor</i> security descriptor.

### -param ObjectsSecurityDescriptor [in, out]

A pointer to a pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure. This security descriptor must be in <a href="/windows/desktop/SecGloss/s-gly">self-relative</a> form. **The memory for the security descriptor must be allocated from the process heap (GetProcessHeap) with the HeapAlloc function.**




On input, this is the current security descriptor of the private object. The function modifies it to produce the new security descriptor. If necessary, the <b>SetPrivateObjectSecurity</b> function allocates additional memory to produce a larger security descriptor.

### -param GenericMapping [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a> structure that specifies the specific and standard access rights that correspond to each of the generic access rights.

### -param Token [in, optional]

A handle to the <a href="/windows/desktop/SecGloss/a-gly">access token</a> for the client on whose behalf the private object's security is being modified. This parameter is required to ensure that the client has provided a legitimate value for a new owner <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID). The token must be open for TOKEN_QUERY access.

## -returns

If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function is intended for use by resource managers only. To implement the standard access control semantics for updating security descriptors, a resource manager should verify that the following conditions are met before calling <b>SetPrivateObjectSecurity</b>:

<ul>
<li>If the object's owner is being set, the calling <a href="/windows/desktop/SecGloss/p-gly">process</a> must have either WRITE_OWNER permission or be the object's owner.</li>
<li>If the object's <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) is being set, the calling process must have either WRITE_DAC permission or be the object's owner.</li>
<li>If the object's <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) is being set, the SE_SECURITY_NAME privilege must be enabled for the calling process.</li>
</ul>
If the preceding conditions are not met, a call to this function does not fail; however, standard access policy is not enforced.

The process calling this function should not be impersonating a client because clients do not typically have appropriate privileges required for underlying token operations.

## -see-also

<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control Overview</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity">CreatePrivateObjectSecurity</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity">DestroyPrivateObjectSecurity</a>



<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity">GetPrivateObjectSecurity</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setfilesecuritya">SetFileSecurity</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity">SetKernelObjectSecurity</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurityex">SetPrivateObjectSecurityEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity">SetUserObjectSecurity</a>