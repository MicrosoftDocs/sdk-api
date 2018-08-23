---
UID: NF:aclapi.SetSecurityInfo
title: SetSecurityInfo function
author: windows-sdk-content
description: Sets specified security information in the security descriptor of a specified object. The caller identifies the object by a handle.
old-location: security\setsecurityinfo.htm
old-project: secauthz
ms.assetid: f1781ba9-81eb-46f9-b530-c390b67d65de
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: SetSecurityInfo, SetSecurityInfo function [Security], _win32_setsecurityinfo, aclapi/SetSecurityInfo, security.setsecurityinfo
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
 - SetSecurityInfo
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
---

# SetSecurityInfo function


## -description


The <b>SetSecurityInfo</b> function sets specified security information in the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> of a specified object. The caller identifies the object by a handle. 

To set the SACL of an object, the caller must have the <b>SE_SECURITY_NAME</b> privilege enabled.


## -parameters




### -param handle [in]

A handle to the object for which to set security information.


### -param ObjectType [in]

A member of the 
<a href="https://msdn.microsoft.com/1dee5e3d-0d41-4717-811b-7e05b4deb55f">SE_OBJECT_TYPE</a> enumeration that indicates the type of object identified by the <i>handle</i> parameter.


### -param SecurityInfo [in]

A set of 
bit flags that indicate the type of security information to set. This parameter can be a combination of the 
<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a> bit flags.


### -param psidOwner [in, optional]

A pointer to a SID that identifies the owner of the object. The SID must be one that can be assigned as the owner SID of a security descriptor. The <i>SecurityInfo</i> parameter must include the OWNER_SECURITY_INFORMATION flag. This parameter can be <b>NULL</b> if you are not setting the owner SID.


### -param psidGroup [in, optional]

A pointer to a SID that identifies the primary group of the object. The <i>SecurityInfo</i> parameter must include the GROUP_SECURITY_INFORMATION flag. This parameter can be <b>NULL</b> if you are not setting the primary group SID.


### -param pDacl [in, optional]

A pointer to the new DACL for the object. This parameter is ignored unless the value of the <i>SecurityInfo</i> parameter includes the <b>DACL_SECURITY_INFORMATION</b> flag.  If the value of the <i>SecurityInfo</i> parameter includes the <b>DACL_SECURITY_INFORMATION</b> flag and the value of this parameter is set to <b>NULL</b>, full access to the object is granted to everyone. For information about <b>null</b> DACLs, see <a href="https://msdn.microsoft.com/f8ec202f-4f34-4123-8f3c-cfc5960b4dc2">Creating a DACL</a>.


### -param pSacl [in, optional]

A pointer to the new SACL for the object. The <i>SecurityInfo</i> parameter must include any of the following flags: SACL_SECURITY_INFORMATION, LABEL_SECURITY_INFORMATION, ATTRIBUTE_SECURITY_INFORMATION, SCOPE_SECURITY_INFORMATION, or BACKUP_SECURITY_INFORMATION. If setting SACL_SECURITY_INFORMATION or SCOPE_SECURITY_INFORMATION, the caller must have the SE_SECURITY_NAME privilege enabled. This parameter can be <b>NULL</b> if you are not setting the SACL.


## -returns



If the function succeeds, the function returns ERROR_SUCCESS.

If the function fails, it returns a nonzero error code defined in WinError.h.




## -remarks



If you are setting the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL) or any elements in the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) of an object, the system automatically propagates any inheritable <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs) to existing child objects, according to the 
<a href="https://msdn.microsoft.com/08f76aaa-8379-4ba8-9735-7568001bcd53">ACE inheritance rules</a>.


You can use the <b>SetSecurityInfo</b> function with the following types of objects:

<ul>
<li>Local or remote files or directories on an NTFS</li>
<li>Named pipes</li>
<li>Local or remote printers</li>
<li>Local or remote Windows services</li>
<li>Network shares</li>
<li>Registry keys</li>
<li>Semaphores, events, mutexes, and waitable timers</li>
<li>Processes, threads, jobs, and file-mapping objects</li>
<li>Window stations and desktops</li>
<li>Directory service objects</li>
</ul>


The <b>SetSecurityInfo</b> function does not reorder access-allowed or access-denied ACEs based on the preferred order. When propagating inheritable ACEs to existing child objects, <b>SetSecurityInfo</b> puts inherited ACEs in order after all of the noninherited ACEs in the DACLs of the child objects.

<div class="alert"><b>Note</b>  If share access to the children of the object is not available, this function will not propagate unprotected ACEs to the children. For example, if a directory is opened with exclusive access, the operating system will not propagate unprotected ACEs to the subdirectories or files of that directory when the security on the directory is changed.</div>
<div> </div>
<div class="alert"><b>Warning</b>  If the supplied <i>handle</i> was opened with an <a href="https://msdn.microsoft.com/f115ee54-3333-4109-8004-d71904a7a943">ACCESS_MASK</a> value of <b>MAXIMUM_ALLOWED</b>, then the <b>SetSecurityInfo</b> function will not propagate ACEs to children.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a>



<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/11f2119b-5314-4fa1-8016-9c01f79d037d">GetNamedSecurityInfo</a>



<a href="https://msdn.microsoft.com/64767a6b-cd79-4e02-881a-706a078ff446">GetSecurityInfo</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a>



<a href="https://msdn.microsoft.com/1dee5e3d-0d41-4717-811b-7e05b4deb55f">SE_OBJECT_TYPE</a>



<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>



<a href="https://msdn.microsoft.com/70fbba50-2576-4857-a955-119fb12bf7b6">SetNamedSecurityInfo</a>
 

 

