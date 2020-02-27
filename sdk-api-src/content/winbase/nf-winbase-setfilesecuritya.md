---
UID: NF:winbase.SetFileSecurityA
title: SetFileSecurityA function (winbase.h)
description: Sets the security of a file or directory object.
old-location: security\setfilesecurity.htm
tech.root: SecAuthZ
ms.assetid: 27766c97-7ac5-40fc-b798-7cd07e496c0d
ms.date: 12/05/2018
ms.keywords: SetFileSecurity, SetFileSecurity function [Security], SetFileSecurityA, SetFileSecurityW, _win32_setfilesecurity, security.setfilesecurity, winbase/SetFileSecurity, winbase/SetFileSecurityA, winbase/SetFileSecurityW
f1_keywords:
- winbase/SetFileSecurity
dev_langs:
- c++
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetFileSecurityW (Unicode) and SetFileSecurityA (ANSI)
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
- AdvApi32Legacy.dll
- API-Ms-Win-Security-Base-Ansi-L1-1-0.dll
- API-MS-Win-Security-Base-L1-2-1.dll
api_name:
- SetFileSecurity
- SetFileSecurityA
- SetFileSecurityW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetFileSecurityA function


## -description


The <b>SetFileSecurity</b> function sets the security of a file or directory object.

This function is obsolete. Use the <a href="https://docs.microsoft.com/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa">SetNamedSecurityInfo</a> function instead.


## -parameters




### -param lpFileName [in]

A pointer to a null-terminated string that specifies the file or directory for which security is set. Note that security applied to a directory is not inherited by its children.


### -param SecurityInformation [in]

Specifies a 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> structure that identifies the contents of the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security descriptor</a> pointed to by the <i>pSecurityDescriptor</i> parameter.


### -param pSecurityDescriptor [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure.


## -returns



If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The <b>SetFileSecurity</b> function is successful only if the following conditions are met:

<ul>
<li>If the owner of the object is being set, the calling <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">process</a> must have either WRITE_OWNER permission or be the owner of the object.</li>
<li>If the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) of the object is being set, the calling process must have either WRITE_DAC permission or be the owner of the object.</li>
<li>If the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) of the object is being set, the SE_SECURITY_NAME privilege must be enabled for the calling process.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-getfilesecuritya">GetFileSecurity</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity">SetKernelObjectSecurity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa">SetNamedSecurityInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity">SetPrivateObjectSecurity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity">SetUserObjectSecurity</a>
 

 

