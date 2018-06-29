---
UID: NF:winuser.GetUserObjectSecurity
title: GetUserObjectSecurity function
author: windows-sdk-content
description: Retrieves security information for the specified user object.
old-location: security\getuserobjectsecurity.htm
old-project: SecAuthZ
ms.assetid: 998c2520-7833-4efd-a794-b13b528f0485
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetUserObjectSecurity, GetUserObjectSecurity function [Security], _win32_getuserobjectsecurity, security.getuserobjectsecurity, winuser/GetUserObjectSecurity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
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
tech.root: 
req.typenames: POINTER_DEVICE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-l1-1-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - GetUserObjectSecurity
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetUserObjectSecurity function


## -description


The <b>GetUserObjectSecurity</b> function retrieves security information for the specified user object.


## -parameters




### -param hObj [in]

A handle to the user object for which to return security information.


### -param pSIRequested [in]

A pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a> value that specifies the security information being requested.


### -param pSID

TBD


### -param nLength [in]

The length, in bytes, of the buffer pointed to by the <i>pSD</i> parameter.


### -param lpnLengthNeeded [out]

A pointer to a variable to receive the number of bytes required to store the complete <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a>. If this variable's value is greater than the value of the <i>nLength</i> parameter when the function returns, the function returns <b>FALSE</b> and none of the security descriptor is copied to the buffer. Otherwise, the entire security descriptor is copied.


#### - pSD [in, out, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure in <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">self-relative</a> format that contains the requested information when the function returns. This buffer must be aligned on a 4-byte boundary. 



					


## -returns




						If the function succeeds, the function returns nonzero.
						

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To read the owner, group, or <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL) from the user object's security descriptor, the calling <a href="https://msdn.microsoft.com/library/windows/hardware/dn756307">process</a> must have been granted READ_CONTROL access when the handle was opened.

To read the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) from the security descriptor, the calling process must have been granted ACCESS_SYSTEM_SECURITY access when the handle was opened. The correct way to get this access is to enable the SE_SECURITY_NAME privilege in the caller's current token, open the handle for ACCESS_SYSTEM_SECURITY access, and then disable the privilege.


#### Examples

For an example that uses this function, see <a href="https://msdn.microsoft.com/9e9ed9b7-ea23-4dec-8b92-a86aa81267ab">Starting an Interactive Client Process</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/5f4832b6-5cf5-4050-9e20-56674f2e2cb1">CreatePrivateObjectSecurity</a>



<a href="https://msdn.microsoft.com/276e9657-5729-48cb-9531-14bfd08b7868">GetKernelObjectSecurity</a>



<a href="https://msdn.microsoft.com/3e93c0a0-e449-4df1-812b-c3fb0dfe9c19">GetPrivateObjectSecurity</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="https://msdn.microsoft.com/library/Aa373557(v=VS.85).aspx">Low-level Access Control Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a>



<a href="https://msdn.microsoft.com/219e41b8-9ac7-4747-a585-b6b9df6a1c9c">SetUserObjectSecurity</a>
 

 

