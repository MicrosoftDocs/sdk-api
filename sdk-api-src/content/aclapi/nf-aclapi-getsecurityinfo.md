---
UID: NF:aclapi.GetSecurityInfo
title: GetSecurityInfo function (aclapi.h)
description: Retrieves a copy of the security descriptor for an object specified by a handle.
helpviewer_keywords: ["GetSecurityInfo","GetSecurityInfo function [Security]","_win32_getsecurityinfo","aclapi/GetSecurityInfo","security.getsecurityinfo"]
old-location: security\getsecurityinfo.htm
tech.root: security
ms.assetid: 64767a6b-cd79-4e02-881a-706a078ff446
ms.date: 12/05/2018
ms.keywords: GetSecurityInfo, GetSecurityInfo function [Security], _win32_getsecurityinfo, aclapi/GetSecurityInfo, security.getsecurityinfo
req.header: aclapi.h
req.include-header: 
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetSecurityInfo
 - aclapi/GetSecurityInfo
dev_langs:
 - c++
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
---

# GetSecurityInfo function


## -description

The <b>GetSecurityInfo</b> function retrieves a copy of the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> for an object specified by a handle.

## -parameters

### -param handle [in]

A handle to the object from which to retrieve security information.

### -param ObjectType [in]

<a href="/windows/desktop/api/accctrl/ne-accctrl-se_object_type">SE_OBJECT_TYPE</a> enumeration value that indicates the type of object.

### -param SecurityInfo [in]

A set of 
bit flags that indicate the type of security information to retrieve. This parameter can be a combination of the 
<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> bit flags.

### -param ppsidOwner [out, optional]

A pointer to a variable that receives a pointer to the owner SID in the security descriptor returned in <i>ppSecurityDescriptor</i>. The returned pointer is valid only if you set the OWNER_SECURITY_INFORMATION flag. This parameter can be <b>NULL</b> if you do not need the owner SID.

### -param ppsidGroup [out, optional]

A pointer to a variable that receives a pointer to the primary group SID in the returned <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a>. The returned pointer is valid only if you set the GROUP_SECURITY_INFORMATION flag. This parameter can be <b>NULL</b> if you do not need the group SID.

### -param ppDacl [out, optional]

A pointer to a variable that receives a pointer to the DACL in the returned security descriptor. The returned pointer is valid only if you set the DACL_SECURITY_INFORMATION flag. This parameter can be <b>NULL</b> if you do not need the DACL.

### -param ppSacl [out, optional]

A pointer to a variable that receives a pointer to the SACL in the returned security descriptor. The returned pointer is valid only if you set the SACL_SECURITY_INFORMATION flag. This parameter can be <b>NULL</b> if you do not need the SACL.

### -param ppSecurityDescriptor [out, optional]

A pointer to a variable that receives a pointer to the security descriptor of the object. When you have finished using the pointer,  free the returned buffer by calling the 
<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.

This parameter is required if any one of the <i>ppsidOwner</i>, <i>ppsidGroup</i>, <i>ppDacl</i>, or <i>ppSacl</i> parameters is not <b>NULL</b>.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in WinError.h.

## -remarks

If the <i>ppsidOwner</i>, <i>ppsidGroup</i>, <i>ppDacl</i>, and <i>ppSacl</i> parameters are non-<b>NULL</b>, and the <i>SecurityInfo</i> parameter specifies that they be retrieved from the object, those parameters will point to the corresponding parameters in the security descriptor returned in <i>ppSecurityDescriptor</i>.

To read the owner, group, or DACL from the object's security descriptor, the calling process must have been granted READ_CONTROL access when the handle was opened. To get READ_CONTROL access, the caller must be the owner of the object or the object's DACL must grant the access.

To read the SACL from the security descriptor, the calling process must have been granted ACCESS_SYSTEM_SECURITY access when the handle was opened. The proper way to get this access is to enable the SE_SECURITY_NAME privilege in the caller's current token, open the handle for ACCESS_SYSTEM_SECURITY access, and then disable the privilege. For information about the security implications of enabling  privileges, see <a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.

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
     <a href="/windows/desktop/SecAuthZ/finding-the-owner-of-a-file-object-in-c--">Finding the Owner of a File Object</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa">GetNamedSecurityInfo</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>



<a href="/windows/desktop/SecAuthZ/authorization-constants">Privilege Constants</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>



<a href="/windows/desktop/api/accctrl/ne-accctrl-se_object_type">SE_OBJECT_TYPE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa">SetNamedSecurityInfo</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo">SetSecurityInfo</a>