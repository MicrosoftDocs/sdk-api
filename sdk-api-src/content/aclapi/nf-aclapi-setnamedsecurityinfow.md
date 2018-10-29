---
UID: NF:aclapi.SetNamedSecurityInfoW
title: SetNamedSecurityInfoW function
author: windows-sdk-content
description: Sets specified security information in the security descriptor of a specified object.
old-location: security\setnamedsecurityinfo.htm
tech.root: SecAuthZ
ms.assetid: 70fbba50-2576-4857-a955-119fb12bf7b6
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: SetNamedSecurityInfo, SetNamedSecurityInfo function [Security], SetNamedSecurityInfoA, SetNamedSecurityInfoW, _win32_setnamedsecurityinfo, aclapi/SetNamedSecurityInfo, aclapi/SetNamedSecurityInfoA, aclapi/SetNamedSecurityInfoW, security.setnamedsecurityinfo
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
req.unicode-ansi: SetNamedSecurityInfoW (Unicode) and SetNamedSecurityInfoA (ANSI)
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
 - SetNamedSecurityInfo
 - SetNamedSecurityInfoA
 - SetNamedSecurityInfoW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetNamedSecurityInfoW function


## -description


The <b>SetNamedSecurityInfo</b> function sets specified security information in the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> of a specified object. The caller identifies the object by name.


## -parameters




### -param pObjectName [in]

A pointer to a <b>null</b>-terminated string that specifies the name of the object for which to set security information. This can be the name of a local or remote file or directory on an NTFS file system, network share, registry key, semaphore, event, mutex, file mapping, or waitable timer. 




For descriptions of the string formats for the different object types, see 
<a href="https://msdn.microsoft.com/1dee5e3d-0d41-4717-811b-7e05b4deb55f">SE_OBJECT_TYPE</a>.


### -param ObjectType [in]

A value of the <a href="https://msdn.microsoft.com/1dee5e3d-0d41-4717-811b-7e05b4deb55f">SE_OBJECT_TYPE</a> enumeration that indicates the type of object named by the <i>pObjectName</i> parameter.


### -param SecurityInfo [in]

A set of 
bit flags that indicate the type of security information to set. This parameter can be a combination of the <a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a> bit flags.


### -param psidOwner [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure that identifies the owner of the object. If the caller does not have the <b>SeRestorePrivilege</b> constant (see <a href="https://msdn.microsoft.com/973796a6-bc2e-4e64-92db-5e17b9c25460">Privilege Constants</a>), this <b>SID</b> must be contained in the caller's token, and must have the <b>SE_GROUP_OWNER</b> permission enabled. The <i>SecurityInfo</i> parameter must include the OWNER_SECURITY_INFORMATION flag. To set the owner, the caller must have WRITE_OWNER access to the object or have the SE_TAKE_OWNERSHIP_NAME privilege enabled. If you are not setting the owner <b>SID</b>, this parameter can be <b>NULL</b>.


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



 If you are setting the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL) or any elements in the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) of an object, the system automatically propagates any inheritable <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs) to existing child objects, according to the 
<a href="https://msdn.microsoft.com/08f76aaa-8379-4ba8-9735-7568001bcd53">rules of inheritance</a>.

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

This function transfers information in <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">plaintext</a>. The information transferred by this function is signed unless signing has been turned off for the system, but no encryption is performed.  

When you update access rights of a folder indicated by an UNC   path, for example \\Test\TestFolder, the original inherited ACE is removed and the full volume path is not included.


#### Examples

For an example that uses this function, see <a href="https://msdn.microsoft.com/0c168bb7-996f-42a8-96cd-2ba7870a3333">Modifying the ACLs of an Object</a> or <a href="https://msdn.microsoft.com/0b309ac9-177d-425f-8b78-71fe73e41979">Taking Object Ownership</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a>



<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/11f2119b-5314-4fa1-8016-9c01f79d037d">GetNamedSecurityInfo</a>



<a href="https://msdn.microsoft.com/64767a6b-cd79-4e02-881a-706a078ff446">GetSecurityInfo</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a>



<a href="https://msdn.microsoft.com/1dee5e3d-0d41-4717-811b-7e05b4deb55f">SE_OBJECT_TYPE</a>



<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>



<a href="https://msdn.microsoft.com/f1781ba9-81eb-46f9-b530-c390b67d65de">SetSecurityInfo</a>
 

 

