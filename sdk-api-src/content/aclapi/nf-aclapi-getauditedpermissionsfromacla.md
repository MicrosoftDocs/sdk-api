---
UID: NF:aclapi.GetAuditedPermissionsFromAclA
title: GetAuditedPermissionsFromAclA function
author: windows-sdk-content
description: Retrieves the audited access rights for a specified trustee.
old-location: security\getauditedpermissionsfromacl.htm
old-project: secauthz
ms.assetid: 4381fe12-5fb3-4f9c-8daa-261cb1a466ec
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: GetAuditedPermissionsFromAcl, GetAuditedPermissionsFromAcl function [Security], GetAuditedPermissionsFromAclA, GetAuditedPermissionsFromAclW, _win32_getauditedpermissionsfromacl, aclapi/GetAuditedPermissionsFromAcl, aclapi/GetAuditedPermissionsFromAclA, aclapi/GetAuditedPermissionsFromAclW, security.getauditedpermissionsfromacl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: aclapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetAuditedPermissionsFromAclW (Unicode) and GetAuditedPermissionsFromAclA (ANSI)
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
 - API-MS-Win-security-trustee-l1-1-1.dll
 - advapi32legacy.dll
api_name:
 - GetAuditedPermissionsFromAcl
 - GetAuditedPermissionsFromAclA
 - GetAuditedPermissionsFromAclW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
---

# GetAuditedPermissionsFromAclA function


## -description


The <b>GetAuditedPermissionsFromAcl</b> function retrieves the audited access rights for a specified trustee. The audited rights are based on the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs) of a specified <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL). The audited access rights indicate the types of access attempts that cause the system to generate an audit record in the system event log. The audited rights include those that the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff538866">ACL</a> specifies for the trustee or for any groups of which the trustee is a member. In determining the audited rights, the function does not consider the security privileges held by the trustee.


## -parameters




### -param pacl [in]

A pointer to an 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff538866">ACL</a> structure from which to get the trustee's audited access rights.


### -param pTrustee [in]

A pointer to a 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure that identifies the trustee. A trustee can be a user, group, or program (such as a Windows service). You can use a name or a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) to identify a trustee. For information about SID structures, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>.


### -param pSuccessfulAuditedRights [out]

A pointer to an 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540466">ACCESS_MASK</a> structure that receives the successful audit mask for rights audited for the trustee specified by the <i>pTrustee</i> parameter. The system generates an audit record when the trustee successfully uses any of these access rights.


### -param pFailedAuditRights [out]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff540466">ACCESS_MASK</a> structure that receives the failed audit mask for rights audited for the trustee specified by the <i>pTrustee</i> parameter. The system generates an audit record when the trustee fails in an attempt to use any of these rights.


## -returns



If the function succeeds, the function returns ERROR_SUCCESS.

If the function fails, it returns a nonzero error code defined in WinError.h.




## -remarks



The <b>GetAuditedPermissionsFromAcl</b> function checks all system-audit ACEs in the ACL to determine the audited rights for the trustee. For all ACEs that specify audited rights for a group, <b>GetAuditedPermissionsFromAcl</b> enumerates the members of the group to determine whether the trustee is a member. The function returns an error if it cannot enumerate the members of a group.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff540466">ACCESS_MASK</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538844">ACE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538866">ACL</a>



<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/c40973e8-72a9-43a2-9873-ea5c666a094c">GetEffectiveRightsFromAcl</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556771">SYSTEM_AUDIT_ACE</a>



<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a>
 

 

