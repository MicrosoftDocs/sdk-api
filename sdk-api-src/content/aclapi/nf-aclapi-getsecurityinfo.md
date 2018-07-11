---
UID: NF:aclapi.GetSecurityInfo
title: GetSecurityInfo function
author: windows-sdk-content
description: Retrieves a copy of the security descriptor for an object specified by a handle.
old-location: security\getsecurityinfo.htm
old-project: secauthz
ms.assetid: 64767a6b-cd79-4e02-881a-706a078ff446
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: GetSecurityInfo, GetSecurityInfo function [Security], _win32_getsecurityinfo, aclapi/GetSecurityInfo, security.getsecurityinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: aclapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
req.typenames: TRUSTEE_W, *PTRUSTEE_W, TRUSTEEW, *PTRUSTEEW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - Ext-MS-Win-AdvAPI32-ntmarta-l1-1-0.dll
 - advapi32legacy.dll
 - api-ms-win-security-provider-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l3-1-0.dll
 - ntmarta.dll
api_name:
 - GetSecurityInfo
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
---

# GetSecurityInfo function


## -description



			The <b>GetSecurityInfo</b> function retrieves a copy of the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> for an object specified by a handle.


## -parameters




### -param handle [in]

A handle to the object from which to retrieve security information.


### -param ObjectType [in]


<a href="https://msdn.microsoft.com/1dee5e3d-0d41-4717-811b-7e05b4deb55f">SE_OBJECT_TYPE</a> enumeration value that indicates the type of object.


### -param SecurityInfo [in]

A set of 
bit flags that indicate the type of security information to retrieve. This parameter can be a combination of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a> bit flags.


### -param ppsidOwner [out, optional]

A pointer to a variable that receives a pointer to the owner SID in the security descriptor returned in <i>ppSecurityDescriptor</i>. The returned pointer is valid only if you set the OWNER_SECURITY_INFORMATION flag. This parameter can be <b>NULL</b> if you do not need the owner SID.


### -param ppsidGroup [out, optional]

A pointer to a variable that receives a pointer to the primary group SID in the returned <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a>. The returned pointer is valid only if you set the GROUP_SECURITY_INFORMATION flag. This parameter can be <b>NULL</b> if you do not need the group SID.


### -param ppDacl [out, optional]

A pointer to a variable that receives a pointer to the DACL in the returned security descriptor. The returned pointer is valid only if you set the DACL_SECURITY_INFORMATION flag. This parameter can be <b>NULL</b> if you do not need the DACL.


### -param ppSacl [out, optional]

A pointer to a variable that receives a pointer to the SACL in the returned security descriptor. The returned pointer is valid only if you set the SACL_SECURITY_INFORMATION flag. This parameter can be <b>NULL</b> if you do not need the SACL.


### -param ppSecurityDescriptor [out, optional]

A pointer to a variable that receives a pointer to the security descriptor of the object. When you have finished using the pointer,  free the returned buffer by calling the 
<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function.

This parameter is required if any one of the <i>ppsidOwner</i>, <i>ppsidGroup</i>, <i>ppDacl</i>, or <i>ppSacl</i> parameters is not <b>NULL</b>.


## -returns




						If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in WinError.h.




## -remarks



If the <i>ppsidOwner</i>, <i>ppsidGroup</i>, <i>ppDacl</i>, and <i>ppSacl</i> parameters are non-<b>NULL</b>, and the <i>SecurityInfo</i> parameter specifies that they be retrieved from the object, those parameters will point to the corresponding parameters in the security descriptor returned in <i>ppSecurityDescriptor</i>.

To read the owner, group, or DACL from the object's security descriptor, the calling process must have been granted READ_CONTROL access when the handle was opened. To get READ_CONTROL access, the caller must be the owner of the object or the object's DACL must grant the access.

To read the SACL from the security descriptor, the calling process must have been granted ACCESS_SYSTEM_SECURITY access when the handle was opened. The proper way to get this access is to enable the SE_SECURITY_NAME privilege in the caller's current token, open the handle for ACCESS_SYSTEM_SECURITY access, and then disable the privilege. For information about the security implications of enabling  privileges, see <a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.

You can use the <b>GetSecurityInfo</b> function with the following types of objects:

<ul>
<li>Local or remote files or directories on an NTFS file system</li>
<li>Named pipes</li>
<li>Local or remote printers</li>
<li>Local or remote Windows services</li>
<li>Network shares</li>
<li>Registry keys</li>
<li>Semaphores, events, mutexes, and waitable timers</li>
<li>Processes, threads, jobs, and file-mapping objects</li>
<li>Interactive service window stations and desktops</li>
<li>Directory service objects</li>
</ul>
This function does not handle race conditions. If your thread calls this function at the approximate time that another thread changes the object's security descriptor, then this function could fail.


#### Examples


     For an example that uses this function, see 
     <a href="https://msdn.microsoft.com/b0dbc785-58a7-4f39-ab39-b96abece5b93">Finding the Owner of a File Object</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538866">ACL</a>



<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/11f2119b-5314-4fa1-8016-9c01f79d037d">GetNamedSecurityInfo</a>



<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>



<a href="authorization_constants.htm">Privilege Constants</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a>



<a href="https://msdn.microsoft.com/1dee5e3d-0d41-4717-811b-7e05b4deb55f">SE_OBJECT_TYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>



<a href="https://msdn.microsoft.com/70fbba50-2576-4857-a955-119fb12bf7b6">SetNamedSecurityInfo</a>



<a href="https://msdn.microsoft.com/f1781ba9-81eb-46f9-b530-c390b67d65de">SetSecurityInfo</a>
 

 

