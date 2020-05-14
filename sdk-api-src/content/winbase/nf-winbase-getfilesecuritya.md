---
UID: NF:winbase.GetFileSecurityA
title: GetFileSecurityA function (winbase.h)
description: Obtains specified information about the security of a file or directory. The information obtained is constrained by the caller's access rights and privileges.helpviewer_keywords: ["GetFileSecurity","GetFileSecurity function [Security]","GetFileSecurityA","GetFileSecurityW","_win32_getfilesecurity","security.getfilesecurity","winbase/GetFileSecurity","winbase/GetFileSecurityA","winbase/GetFileSecurityW"]
old-location: security\getfilesecurity.htm
tech.root: SecAuthZ
ms.assetid: 4043b76b-76b9-4111-8a29-a808b2412be0
ms.date: 12/05/2018
ms.keywords: GetFileSecurity, GetFileSecurity function [Security], GetFileSecurityA, GetFileSecurityW, _win32_getfilesecurity, security.getfilesecurity, winbase/GetFileSecurity, winbase/GetFileSecurityA, winbase/GetFileSecurityW
f1_keywords:
- winbase/GetFileSecurity
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
req.unicode-ansi: GetFileSecurityW (Unicode) and GetFileSecurityA (ANSI)
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
- GetFileSecurity
- GetFileSecurityA
- GetFileSecurityW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetFileSecurityA function


## -description


The <b>GetFileSecurity</b> function obtains specified information about the security of a file or directory. The information obtained is constrained by the caller's access rights and <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">privileges</a>.

The <a href="https://docs.microsoft.com/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa">GetNamedSecurityInfo</a> function provides functionality similar to <b>GetFileSecurity</b> for files as well as other types of objects.


## -parameters




### -param lpFileName [in]

A pointer to a null-terminated string that specifies the file or directory for which security information is retrieved.


### -param RequestedInformation [in]

A 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> value that identifies the security information being requested.


### -param pSecurityDescriptor [out, optional]

A pointer to a buffer that receives a copy of the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security descriptor</a> of the object specified by the <i>lpFileName</i> parameter. The calling <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">process</a> must have permission to view the specified aspects of the object's security status. The 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure is returned in <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">self-relative security descriptor</a> format.


### -param nLength [in]

Specifies the size, in bytes, of the buffer pointed to by the <i>pSecurityDescriptor</i> parameter.


### -param lpnLengthNeeded [out]

A pointer to the variable that receives the number of bytes necessary to store the complete <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security descriptor</a>. If the returned number of bytes is less than or equal to <i>nLength</i>, the entire security descriptor is returned in the output buffer; otherwise, none of the descriptor is returned.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



To read the owner, group, or <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">DACL</a> from the security descriptor for the specified file or directory, the DACL for the file or directory must grant READ_CONTROL access to the caller, or the caller must be the owner of the file or directory.

To read the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">SACL</a> of a file or directory, the SE_SECURITY_NAME privilege must be enabled for the calling process.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity">GetKernelObjectSecurity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa">GetNamedSecurityInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity">GetPrivateObjectSecurity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity">GetUserObjectSecurity</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-setfilesecuritya">SetFileSecurity</a>
 

 

