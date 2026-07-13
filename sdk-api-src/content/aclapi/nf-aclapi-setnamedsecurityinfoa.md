---
UID: NF:aclapi.SetNamedSecurityInfoA
title: SetNamedSecurityInfoA function (aclapi.h)
description: Sets specified security information in the security descriptor of a specified object. (ANSI)
helpviewer_keywords: ["SetNamedSecurityInfoA", "aclapi/SetNamedSecurityInfoA"]
old-location: security\setnamedsecurityinfo.htm
tech.root: security
ms.assetid: 70fbba50-2576-4857-a955-119fb12bf7b6
ms.date: 12/05/2018
ms.keywords: SetNamedSecurityInfo, SetNamedSecurityInfo function [Security], SetNamedSecurityInfoA, SetNamedSecurityInfoW, _win32_setnamedsecurityinfo, aclapi/SetNamedSecurityInfo, aclapi/SetNamedSecurityInfoA, aclapi/SetNamedSecurityInfoW, security.setnamedsecurityinfo
req.header: aclapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetNamedSecurityInfoW (Unicode) and SetNamedSecurityInfoA (ANSI)
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
 - SetNamedSecurityInfoA
 - aclapi/SetNamedSecurityInfoA
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
 - SetNamedSecurityInfo
 - SetNamedSecurityInfoA
 - SetNamedSecurityInfoW
---

# SetNamedSecurityInfoA function


## -description

The <b>SetNamedSecurityInfo</b> function sets specified security information in the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> of a specified object. The caller identifies the object by name.

## -parameters

### -param pObjectName [in]

A pointer to a <b>null</b>-terminated string that specifies the name of the object for which to set security information. This can be the name of a local or remote file or directory on an NTFS file system, network share, registry key, semaphore, event, mutex, file mapping, or waitable timer. 




For descriptions of the string formats for the different object types, see 
<a href="/windows/desktop/api/accctrl/ne-accctrl-se_object_type">SE_OBJECT_TYPE</a>.

### -param ObjectType [in]

A value of the <a href="/windows/desktop/api/accctrl/ne-accctrl-se_object_type">SE_OBJECT_TYPE</a> enumeration that indicates the type of object named by the <i>pObjectName</i> parameter.

### -param SecurityInfo [in]

A set of 
bit flags that indicate the type of security information to set. This parameter can be a combination of the <a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> bit flags.

### -param psidOwner [in, optional]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure that identifies the owner of the object. If the caller does not have the <b>SeRestorePrivilege</b> constant (see <a href="/windows/desktop/SecAuthZ/privilege-constants">Privilege Constants</a>), this <b>SID</b> must be contained in the caller's token, and must have the <b>SE_GROUP_OWNER</b> permission enabled. The <i>SecurityInfo</i> parameter must include the OWNER_SECURITY_INFORMATION flag. To set the owner, the caller must have WRITE_OWNER access to the object or have the SE_TAKE_OWNERSHIP_NAME privilege enabled. If you are not setting the owner <b>SID</b>, this parameter can be <b>NULL</b>.

### -param psidGroup [in, optional]

A pointer to a SID that identifies the primary group of the object. The <i>SecurityInfo</i> parameter must include the GROUP_SECURITY_INFORMATION flag. If you are not setting the primary group SID, this parameter can be <b>NULL</b>.

### -param pDacl [in, optional]

A pointer to the new DACL for the object. The <i>SecurityInfo</i> parameter must include the DACL_SECURITY_INFORMATION flag. The caller must have WRITE_DAC access to the object or be the owner of the object. If you are not setting the DACL, this parameter can be <b>NULL</b>.

### -param pSacl [in, optional]

A pointer to the new SACL for the object. The <i>SecurityInfo</i> parameter must include any of the following flags: SACL_SECURITY_INFORMATION, LABEL_SECURITY_INFORMATION, ATTRIBUTE_SECURITY_INFORMATION, SCOPE_SECURITY_INFORMATION, or BACKUP_SECURITY_INFORMATION. 



If setting SACL_SECURITY_INFORMATION or SCOPE_SECURITY_INFORMATION, the caller must have the SE_SECURITY_NAME privilege enabled. If you are not setting the SACL, this parameter can be <b>NULL</b>.

## -returns

If the function succeeds, the function returns ERROR_SUCCESS.

If the function fails, it returns a nonzero error code defined in WinError.h.

## -remarks

 If you are setting the <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) or any elements in the <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) of an object, the system automatically propagates any inheritable <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs) to existing child objects, according to the 
<a href="/windows/desktop/SecAuthZ/ace-inheritance-rules">rules of inheritance</a>.

You can use the <b>SetNamedSecurityInfo</b> function with the following types of objects:

<ul>
<li>Local or remote files or directories on an NTFS</li>
<li>Local or remote printers</li>
<li>Local or remote Windows services</li>
<li>Network shares</li>
<li>Registry keys</li>
<li>Semaphores, events, mutexes, and waitable timers</li>
<li>File-mapping objects</li>
<li>Directory service objects</li>
</ul>
The <b>SetNamedSecurityInfo</b> function does not reorder access-allowed or access-denied ACEs based on the preferred order. When propagating inheritable ACEs to existing child objects, <b>SetNamedSecurityInfo</b> puts inherited ACEs in order after all of the noninherited ACEs in the DACLs of the child objects.

This function transfers information in <a href="/windows/desktop/SecGloss/p-gly">plaintext</a>. The information transferred by this function is signed unless signing has been turned off for the system, but no encryption is performed.  

When you update access rights of a folder indicated by an UNC   path, for example \\Test\TestFolder, the original inherited ACE is removed and the full volume path is not included.


#### Examples

For an example that uses this function, see <a href="/windows/desktop/SecAuthZ/modifying-the-acls-of-an-object-in-c--">Modifying the ACLs of an Object</a> or <a href="/windows/desktop/SecAuthZ/taking-object-ownership-in-c--">Taking Object Ownership</a>.

<div class="code"></div>




> [!NOTE]
> The aclapi.h header defines SetNamedSecurityInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa">GetNamedSecurityInfo</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo">GetSecurityInfo</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>



<a href="/windows/desktop/api/accctrl/ne-accctrl-se_object_type">SE_OBJECT_TYPE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo">SetSecurityInfo</a>
