---
UID: NF:aclapi.GetNamedSecurityInfoA
title: GetNamedSecurityInfoA function
author: windows-sdk-content
description: Retrieves a copy of the security descriptor for an object specified by name.
old-location: security\getnamedsecurityinfo.htm
old-project: secauthz
ms.assetid: 11f2119b-5314-4fa1-8016-9c01f79d037d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetNamedSecurityInfo, GetNamedSecurityInfo function [Security], GetNamedSecurityInfoA, GetNamedSecurityInfoW, _win32_getnamedsecurityinfo, aclapi/GetNamedSecurityInfo, aclapi/GetNamedSecurityInfoA, aclapi/GetNamedSecurityInfoW, security.getnamedsecurityinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: aclapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetNamedSecurityInfoW (Unicode) and GetNamedSecurityInfoA (ANSI)
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
 - GetNamedSecurityInfo
 - GetNamedSecurityInfoA
 - GetNamedSecurityInfoW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
---

# GetNamedSecurityInfoA function


## -description


The <b>GetNamedSecurityInfo</b> function retrieves a copy of the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> for an object specified by name.


## -parameters




### -param pObjectName [in]

A pointer to a null-terminated string that specifies the name of the object from which to retrieve security information. For descriptions of the string formats for the different object types, see 
<a href="https://msdn.microsoft.com/1dee5e3d-0d41-4717-811b-7e05b4deb55f">SE_OBJECT_TYPE</a>.


### -param ObjectType [in]

Specifies a value from the <a href="https://msdn.microsoft.com/1dee5e3d-0d41-4717-811b-7e05b4deb55f">SE_OBJECT_TYPE</a> enumeration that indicates the type of object named by the <i>pObjectName</i> parameter.


### -param SecurityInfo [in]

A set of 
bit flags that indicate the type of security information to retrieve. This parameter can be a combination of the 
<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a> bit flags.


### -param ppsidOwner [out, optional]

A pointer to a variable that receives a pointer to the owner SID in the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> returned in <i>ppSecurityDescriptor</i> or <b>NULL</b> if the security descriptor has no owner SID. The returned pointer is valid only if you set the OWNER_SECURITY_INFORMATION flag. Also, this parameter can be <b>NULL</b> if you do not need the owner SID.


### -param ppsidGroup [out, optional]

A pointer to a variable that receives a pointer to the primary group SID in the returned security descriptor or <b>NULL</b> if  the security descriptor has no group SID. The returned pointer is valid only if you set the GROUP_SECURITY_INFORMATION flag. Also, this parameter can be <b>NULL</b> if you do not need the group SID.


### -param ppDacl [out, optional]

A pointer to a variable that receives a pointer to the DACL in the returned security descriptor or <b>NULL</b> if the security descriptor has no DACL. The returned pointer is valid only if you set the DACL_SECURITY_INFORMATION flag. Also, this parameter can be <b>NULL</b> if you do not need the DACL.


### -param ppSacl [out, optional]

A pointer to a variable that receives a pointer to the SACL in the returned security descriptor  or <b>NULL</b> if the security descriptor has no SACL. The returned pointer is valid only if you set the SACL_SECURITY_INFORMATION flag. Also, this parameter can be <b>NULL</b> if you do not need the SACL.


### -param ppSecurityDescriptor [out, optional]

A pointer to a variable that receives a pointer to the security descriptor of the object. When you have finished using the pointer,  free the returned buffer by calling the 
<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function.

This parameter is required if any one of the <i>ppsidOwner</i>, <i>ppsidGroup</i>, <i>ppDacl</i>, or <i>ppSacl</i> parameters is not <b>NULL</b>.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in WinError.h.




## -remarks



If any of the <i>ppsidOwner</i>, <i>ppsidGroup</i>, <i>ppDacl</i>, or <i>ppSacl</i> parameters are non-<b>NULL</b>, and the <i>SecurityInfo</i> parameter specifies that they be retrieved from the object, those parameters will point to the corresponding parameters in the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> returned in <i>ppSecurityDescriptor</i>. If the security descriptor does not contain the requested information, the corresponding parameter will be set to  <b>NULL</b>.

To read the owner, group, or DACL from the object's security descriptor, the object's DACL must grant READ_CONTROL access to the caller, or the caller must be the owner of the object.

To read the system access control list of the object, the SE_SECURITY_NAME privilege must be enabled for the calling process. For information about the security implications of  enabling privileges, see <a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.

You can use the <b>GetNamedSecurityInfo</b> function with the following types of objects:

<ul>
<li>Local or remote files or directories on an NTFS file system</li>
<li>Local or remote printers</li>
<li>Local or remote Windows services</li>
<li>Network shares</li>
<li>Registry keys</li>
<li>Semaphores, events, mutexes, and waitable timers</li>
<li>File-mapping objects</li>
<li>Directory service objects</li>
</ul>
This function does not handle race conditions. If your thread calls this function at the approximate time that another thread changes the object's security descriptor, then this function could fail.

This function transfers information in plaintext. The information transferred by this function is signed unless signing has been turned off for the system, but no encryption is performed.  

For more information about controlling access to objects through user accounts, group  accounts, or logon sessions,  see <a href="https://msdn.microsoft.com/dc98b23e-ce42-4d4a-a285-c0b7b5e2a478">How DACLs Control Access to an Object</a>.


#### Examples

For an example that uses <b>GetNamedSecurityInfo</b>, see <a href="https://msdn.microsoft.com/0c168bb7-996f-42a8-96cd-2ba7870a3333">Modifying the ACLs of an Object</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a>



<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/64767a6b-cd79-4e02-881a-706a078ff446">GetSecurityInfo</a>



<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375728(v=VS.85).aspx">Privilege Constants</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a>



<a href="https://msdn.microsoft.com/1dee5e3d-0d41-4717-811b-7e05b4deb55f">SE_OBJECT_TYPE</a>



<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>



<a href="https://msdn.microsoft.com/70fbba50-2576-4857-a955-119fb12bf7b6">SetNamedSecurityInfo</a>



<a href="https://msdn.microsoft.com/f1781ba9-81eb-46f9-b530-c390b67d65de">SetSecurityInfo</a>
 

 

