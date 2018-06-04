---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

