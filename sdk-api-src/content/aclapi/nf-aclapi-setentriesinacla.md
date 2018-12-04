---
UID: NF:aclapi.SetEntriesInAclA
title: SetEntriesInAclA function
author: windows-sdk-content
description: Creates a new access control list (ACL) by merging new access control or audit control information into an existing ACL structure.
old-location: security\setentriesinacl.htm
tech.root: secauthz
ms.assetid: 05960fc1-1ad2-4c19-a65c-62259af5e18c
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: SetEntriesInAcl, SetEntriesInAcl function [Security], SetEntriesInAclA, SetEntriesInAclW, _win32_setentriesinacl, aclapi/SetEntriesInAcl, aclapi/SetEntriesInAclA, aclapi/SetEntriesInAclW, security.setentriesinacl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: aclapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetEntriesInAclW (Unicode) and SetEntriesInAclA (ANSI)
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
 - API-MS-Win-Security-Provider-l1-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-DownLevel-AdvApi32-l3-1-0.dll
 - ntmarta.dll
 - API-MS-Win-Security-Provider-Ansi-L1-1-0.dll
api_name:
 - SetEntriesInAcl
 - SetEntriesInAclA
 - SetEntriesInAclW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetEntriesInAclA function


## -description


The <b>SetEntriesInAcl</b> function creates a new <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL) by merging new access control or audit control information into an existing 
<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a> structure.


## -parameters




### -param cCountOfExplicitEntries [in]

The number of 
<a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structures in the <i>pListOfExplicitEntries</i> array.


### -param pListOfExplicitEntries [in, optional]

A pointer to an array of <a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structures that describe the access control information to merge into the existing ACL.


### -param OldAcl [in, optional]

A pointer to the existing ACL. This parameter can be <b>NULL</b>, in which case, the function creates a new ACL based on the <a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> entries.


### -param NewAcl [out]

A pointer to a variable that receives a pointer to the new ACL. If the function succeeds, you must call the 
<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function to free the returned buffer.


## -returns



If the function succeeds, the function returns ERROR_SUCCESS.

If the function fails, it returns a nonzero error code defined in WinError.h.




## -remarks



Each entry in the array of <a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structures specifies access control or audit control information for a specified trustee. A trustee can be a user, group, or other <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) value, such as a <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon identifier</a> or logon type (for instance, a Windows service or batch job). You can use a name or a SID to identify a trustee.

You can use the <b>SetEntriesInAcl</b> function to modify the list of <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs) in a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL) or a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL). Note that <b>SetEntriesInAcl</b> does not prevent you from mixing access control and audit control information in the same 
<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a>; however, the resulting ACL will contain meaningless entries.

For a DACL, the <b>grfAccessMode</b> member of the 
<a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structure specifies whether to allow, deny, or revoke access rights for the trustee. This member can specify one of the following values:

<ul>
<li>GRANT_ACCESS</li>
<li>SET_ACCESS</li>
<li>DENY_ACCESS</li>
<li>REVOKE_ACCESS</li>
</ul>
 For information about these values, see <a href="https://msdn.microsoft.com/52d1b3a3-eed5-4603-9056-520320da2a52">ACCESS_MODE</a>.

The <b>SetEntriesInAcl</b> function places any new access-denied ACEs at the beginning of the list of ACEs for the new 
<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a>. This function  places any new access-allowed ACEs just before any existing access-allowed ACEs.

For a SACL, the <b>grfAccessMode</b> member of the 
<a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structure can specify the following values:

<ul>
<li>REVOKE_ACCESS</li>
<li>SET_AUDIT_FAILURE</li>
<li>SET_AUDIT_SUCCESS</li>
</ul>
SET_AUDIT_FAILURE and  SET_AUDIT_SUCCESS can be combined. For information about these values, see <a href="https://msdn.microsoft.com/52d1b3a3-eed5-4603-9056-520320da2a52">ACCESS_MODE</a>.

The <b>SetEntriesInAcl</b> function places any new system-audit ACEs at the beginning of the list of ACEs for the new ACL.


#### Examples

For an example that uses this function, see <a href="https://msdn.microsoft.com/0c168bb7-996f-42a8-96cd-2ba7870a3333">Modifying the ACLs of an Object</a> or <a href="https://msdn.microsoft.com/866992a7-95c4-4094-87bb-e6d8eeb24317">Creating a Security Descriptor for a New Object</a> or <a href="https://msdn.microsoft.com/0b309ac9-177d-425f-8b78-71fe73e41979">Taking Object Ownership</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/002a3fa7-02a3-4832-948e-b048f5f5818f">ACCESS_ALLOWED_ACE</a>



<a href="https://msdn.microsoft.com/d76a92d0-ccd0-4e73-98b6-43bcd661134d">ACCESS_DENIED_ACE</a>



<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a>



<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a>



<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>



<a href="https://msdn.microsoft.com/c26b5856-5447-4606-8110-f24a4d235c64">SYSTEM_AUDIT_ACE</a>
 

 

