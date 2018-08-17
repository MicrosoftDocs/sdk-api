---
UID: NF:winbase.GetFileSecurityA
title: GetFileSecurityA function
author: windows-sdk-content
description: Obtains specified information about the security of a file or directory. The information obtained is constrained by the caller's access rights and privileges.
old-location: security\getfilesecurity.htm
old-project: secauthz
ms.assetid: 4043b76b-76b9-4111-8a29-a808b2412be0
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: GetFileSecurity, GetFileSecurity function [Security], GetFileSecurityA, GetFileSecurityW, _win32_getfilesecurity, security.getfilesecurity, winbase/GetFileSecurity, winbase/GetFileSecurityA, winbase/GetFileSecurityW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: PRIORITY_HINT
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
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetFileSecurityA function


## -description


The <b>GetFileSecurity</b> function obtains specified information about the security of a file or directory. The information obtained is constrained by the caller's access rights and <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">privileges</a>.

The <a href="https://msdn.microsoft.com/11f2119b-5314-4fa1-8016-9c01f79d037d">GetNamedSecurityInfo</a> function provides functionality similar to <b>GetFileSecurity</b> for files as well as other types of objects.


## -parameters




### -param lpFileName [in]

A pointer to a null-terminated string that specifies the file or directory for which security information is retrieved.


### -param RequestedInformation [in]

A 
<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a> value that identifies the security information being requested.


### -param pSecurityDescriptor [out, optional]

A pointer to a buffer that receives a copy of the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> of the object specified by the <i>lpFileName</i> parameter. The calling <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a> must have permission to view the specified aspects of the object's security status. The 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure is returned in <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">self-relative security descriptor</a> format.


### -param nLength [in]

Specifies the size, in bytes, of the buffer pointed to by the <i>pSecurityDescriptor</i> parameter.


### -param lpnLengthNeeded [out]

A pointer to the variable that receives the number of bytes necessary to store the complete <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a>. If the returned number of bytes is less than or equal to <i>nLength</i>, the entire security descriptor is returned in the output buffer; otherwise, none of the descriptor is returned.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To read the owner, group, or <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">DACL</a> from the security descriptor for the specified file or directory, the DACL for the file or directory must grant READ_CONTROL access to the caller, or the caller must be the owner of the file or directory.

To read the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">SACL</a> of a file or directory, the SE_SECURITY_NAME privilege must be enabled for the calling process.




## -see-also




<a href="https://msdn.microsoft.com/276e9657-5729-48cb-9531-14bfd08b7868">GetKernelObjectSecurity</a>



<a href="https://msdn.microsoft.com/11f2119b-5314-4fa1-8016-9c01f79d037d">GetNamedSecurityInfo</a>



<a href="https://msdn.microsoft.com/3e93c0a0-e449-4df1-812b-c3fb0dfe9c19">GetPrivateObjectSecurity</a>



<a href="https://msdn.microsoft.com/998c2520-7833-4efd-a794-b13b528f0485">GetUserObjectSecurity</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="authorization_functions.htm">Low-level Access Control Functions</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a>



<a href="https://msdn.microsoft.com/27766c97-7ac5-40fc-b798-7cd07e496c0d">SetFileSecurity</a>
 

 

