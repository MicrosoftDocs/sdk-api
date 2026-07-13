---
UID: NF:aclapi.GetNamedSecurityInfoA
title: GetNamedSecurityInfoA function (aclapi.h)
description: Retrieves a copy of the security descriptor for an object specified by name. (ANSI)
helpviewer_keywords: ["GetNamedSecurityInfoA", "aclapi/GetNamedSecurityInfoA"]
old-location: security\getnamedsecurityinfo.htm
tech.root: security
ms.assetid: 11f2119b-5314-4fa1-8016-9c01f79d037d
ms.date: 12/05/2018
ms.keywords: GetNamedSecurityInfo, GetNamedSecurityInfo function [Security], GetNamedSecurityInfoA, GetNamedSecurityInfoW, _win32_getnamedsecurityinfo, aclapi/GetNamedSecurityInfo, aclapi/GetNamedSecurityInfoA, aclapi/GetNamedSecurityInfoW, security.getnamedsecurityinfo
req.header: aclapi.h
req.include-header: 
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetNamedSecurityInfoA
 - aclapi/GetNamedSecurityInfoA
dev_langs:
 - c++
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
---

# GetNamedSecurityInfoA function


## -description

The <b>GetNamedSecurityInfo</b> function retrieves a copy of the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> for an object specified by name.

## -parameters

### -param pObjectName [in]

A pointer to a null-terminated string that specifies the name of the object from which to retrieve security information. For descriptions of the string formats for the different object types, see 
<a href="/windows/desktop/api/accctrl/ne-accctrl-se_object_type">SE_OBJECT_TYPE</a>.

### -param ObjectType [in]

Specifies a value from the <a href="/windows/desktop/api/accctrl/ne-accctrl-se_object_type">SE_OBJECT_TYPE</a> enumeration that indicates the type of object named by the <i>pObjectName</i> parameter.

### -param SecurityInfo [in]

A set of 
bit flags that indicate the type of security information to retrieve. This parameter can be a combination of the 
<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> bit flags.

### -param ppsidOwner [out, optional]

A pointer to a variable that receives a pointer to the owner SID in the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> returned in <i>ppSecurityDescriptor</i> or <b>NULL</b> if the security descriptor has no owner SID. The returned pointer is valid only if you set the OWNER_SECURITY_INFORMATION flag. Also, this parameter can be <b>NULL</b> if you do not need the owner SID.

### -param ppsidGroup [out, optional]

A pointer to a variable that receives a pointer to the primary group SID in the returned security descriptor or <b>NULL</b> if  the security descriptor has no group SID. The returned pointer is valid only if you set the GROUP_SECURITY_INFORMATION flag. Also, this parameter can be <b>NULL</b> if you do not need the group SID.

### -param ppDacl [out, optional]

A pointer to a variable that receives a pointer to the DACL in the returned security descriptor or <b>NULL</b> if the security descriptor has no DACL. The returned pointer is valid only if you set the DACL_SECURITY_INFORMATION flag. Also, this parameter can be <b>NULL</b> if you do not need the DACL.

### -param ppSacl [out, optional]

A pointer to a variable that receives a pointer to the SACL in the returned security descriptor  or <b>NULL</b> if the security descriptor has no SACL. The returned pointer is valid only if you set the SACL_SECURITY_INFORMATION flag. Also, this parameter can be <b>NULL</b> if you do not need the SACL.

### -param ppSecurityDescriptor [out, optional]

A pointer to a variable that receives a pointer to the security descriptor of the object. When you have finished using the pointer,  free the returned buffer by calling the 
<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.

This parameter is required if any one of the <i>ppsidOwner</i>, <i>ppsidGroup</i>, <i>ppDacl</i>, or <i>ppSacl</i> parameters is not <b>NULL</b>.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in WinError.h.

## -remarks

If any of the <i>ppsidOwner</i>, <i>ppsidGroup</i>, <i>ppDacl</i>, or <i>ppSacl</i> parameters are non-<b>NULL</b>, and the <i>SecurityInfo</i> parameter specifies that they be retrieved from the object, those parameters will point to the corresponding parameters in the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> returned in <i>ppSecurityDescriptor</i>. If the security descriptor does not contain the requested information, the corresponding parameter will be set to  <b>NULL</b>.

To read the owner, group, or DACL from the object's security descriptor, the object's DACL must grant READ_CONTROL access to the caller, or the caller must be the owner of the object.

To read the system access control list of the object, the SE_SECURITY_NAME privilege must be enabled for the calling process. For information about the security implications of  enabling privileges, see <a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.

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

For more information about controlling access to objects through user accounts, group  accounts, or logon sessions,  see <a href="/windows/desktop/SecAuthZ/how-dacls-control-access-to-an-object">How DACLs Control Access to an Object</a>.


#### Examples

For an example that uses <b>GetNamedSecurityInfo</b>, see <a href="/windows/desktop/SecAuthZ/modifying-the-acls-of-an-object-in-c--">Modifying the ACLs of an Object</a>.

<div class="code"></div>




> [!NOTE]
> The aclapi.h header defines GetNamedSecurityInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo">GetSecurityInfo</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>



<a href="/windows/desktop/SecAuthZ/authorization-constants">Privilege Constants</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>



<a href="/windows/desktop/api/accctrl/ne-accctrl-se_object_type">SE_OBJECT_TYPE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa">SetNamedSecurityInfo</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo">SetSecurityInfo</a>
