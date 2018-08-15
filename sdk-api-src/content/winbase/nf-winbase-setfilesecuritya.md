---
UID: NF:winbase.SetFileSecurityA
title: SetFileSecurityA function
author: windows-sdk-content
description: Sets the security of a file or directory object.
old-location: security\setfilesecurity.htm
old-project: secauthz
ms.assetid: 27766c97-7ac5-40fc-b798-7cd07e496c0d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SetFileSecurity, SetFileSecurity function [Security], SetFileSecurityA, SetFileSecurityW, _win32_setfilesecurity, security.setfilesecurity, winbase/SetFileSecurity, winbase/SetFileSecurityA, winbase/SetFileSecurityW
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
req.unicode-ansi: SetFileSecurityW (Unicode) and SetFileSecurityA (ANSI)
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
 - SetFileSecurity
 - SetFileSecurityA
 - SetFileSecurityW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetFileSecurityA function


## -description


The <b>SetFileSecurity</b> function sets the security of a file or directory object.

This function is obsolete. Use the <a href="https://msdn.microsoft.com/70fbba50-2576-4857-a955-119fb12bf7b6">SetNamedSecurityInfo</a> function instead.


## -parameters




### -param lpFileName [in]

A pointer to a null-terminated string that specifies the file or directory for which security is set. Note that security applied to a directory is not inherited by its children.


### -param SecurityInformation [in]

Specifies a 
<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a> structure that identifies the contents of the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> pointed to by the <i>pSecurityDescriptor</i> parameter.


### -param pSecurityDescriptor [in]

A pointer to a 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure.


## -returns



If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>SetFileSecurity</b> function is successful only if the following conditions are met:

<ul>
<li>If the owner of the object is being set, the calling <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a> must have either WRITE_OWNER permission or be the owner of the object.</li>
<li>If the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL) of the object is being set, the calling process must have either WRITE_DAC permission or be the owner of the object.</li>
<li>If the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) of the object is being set, the SE_SECURITY_NAME privilege must be enabled for the calling process.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/4043b76b-76b9-4111-8a29-a808b2412be0">GetFileSecurity</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="authorization_functions.htm">Low-level Access Control Functions</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a>



<a href="https://msdn.microsoft.com/2a70483e-245d-4bc7-b90a-58d143364ce1">SetKernelObjectSecurity</a>



<a href="https://msdn.microsoft.com/70fbba50-2576-4857-a955-119fb12bf7b6">SetNamedSecurityInfo</a>



<a href="https://msdn.microsoft.com/726994c8-7813-4f1a-b7d7-a25e79202c33">SetPrivateObjectSecurity</a>



<a href="https://msdn.microsoft.com/219e41b8-9ac7-4747-a585-b6b9df6a1c9c">SetUserObjectSecurity</a>
 

 

