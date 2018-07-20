---
UID: NF:aclapi.GetExplicitEntriesFromAclW
title: GetExplicitEntriesFromAclW function
author: windows-sdk-content
description: Retrieves an array of structures that describe the access control entries (ACEs) in an access control list (ACL).
old-location: security\getexplicitentriesfromacl.htm
old-project: SecAuthZ
ms.assetid: 186aa6aa-efc3-4f8a-acad-e257da3dac0b
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: GetExplicitEntriesFromAcl, GetExplicitEntriesFromAcl function [Security], GetExplicitEntriesFromAclA, GetExplicitEntriesFromAclW, _win32_getexplicitentriesfromacl, aclapi/GetExplicitEntriesFromAcl, aclapi/GetExplicitEntriesFromAclA, aclapi/GetExplicitEntriesFromAclW, security.getexplicitentriesfromacl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: aclapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetExplicitEntriesFromAclW (Unicode) and GetExplicitEntriesFromAclA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TRUSTEE_W, *PTRUSTEE_W, TRUSTEEW, *PTRUSTEEW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Security-Provider-l1-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-DownLevel-AdvApi32-l3-1-0.dll
 - ntmarta.dll
 - API-MS-Win-Security-Provider-Ansi-L1-1-0.dll
api_name:
 - GetExplicitEntriesFromAcl
 - GetExplicitEntriesFromAclA
 - GetExplicitEntriesFromAclW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
---

# GetExplicitEntriesFromAclW function


## -description



			The <b>GetExplicitEntriesFromAcl</b> function retrieves an array of structures that describe the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs) in an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL).


## -parameters




### -param pacl [in]

A pointer to an 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff538866">ACL</a> structure from which to get 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff538844">ACE</a> information.


### -param pcCountOfExplicitEntries [out]

A pointer to a variable that receives the number of <a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structures returned in the <i>pListOfExplicitEntries</i> array.


### -param pListOfExplicitEntries [out]

A pointer to a variable that receives a pointer to an array of <a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structures that describe the ACEs in the ACL. If the function succeeds, you must call the 
<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function to free the returned buffer.


## -returns




						If the function succeeds, the function returns ERROR_SUCCESS.

If the function fails, it returns a nonzero error code defined in WinError.h.




## -remarks



Each entry in the array of 
<a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structures describes access control information from an 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff538844">ACE</a> for a trustee. A trustee can be a user, group, or program (such as a Windows service).

Each <a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structure specifies a set of access rights and an access mode flag that indicates whether the ACE allows, denies, or audits the specified rights.

For a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL), the access mode flag can be  either GRANT_ACCESS or DENY_ACCESS. For information about these values, see <a href="https://msdn.microsoft.com/52d1b3a3-eed5-4603-9056-520320da2a52">ACCESS_MODE</a>.

For a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL), the access mode flag can be SET_AUDIT_ACCESS, SET_AUDIT_FAILURE, or both. For information about these values, see <a href="https://msdn.microsoft.com/52d1b3a3-eed5-4603-9056-520320da2a52">ACCESS_MODE</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538796">ACCESS_ALLOWED_ACE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538831">ACCESS_DENIED_ACE</a>



<a href="https://msdn.microsoft.com/52d1b3a3-eed5-4603-9056-520320da2a52">ACCESS_MODE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538844">ACE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538866">ACL</a>



<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a>



<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556771">SYSTEM_AUDIT_ACE</a>
 

 

