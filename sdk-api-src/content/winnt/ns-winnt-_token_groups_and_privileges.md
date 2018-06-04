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

# _TOKEN_GROUPS_AND_PRIVILEGES structure


## -description


The <b>TOKEN_GROUPS_AND_PRIVILEGES</b> structure contains information about the group <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs) and privileges in an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a>.


## -struct-fields




### -field SidCount

Number of SIDs in the access token.


### -field SidLength

Length, in bytes, required to hold all of the user SIDs and the account SID for the group.


### -field Sids

A pointer to an array of 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556742">SID_AND_ATTRIBUTES</a> structures that contain a set of SIDs and corresponding attributes.

The <b>Attributes</b> members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556742">SID_AND_ATTRIBUTES</a> structures can have the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SE_GROUP_ENABLED"></a><a id="se_group_enabled"></a><dl>
<dt><b>SE_GROUP_ENABLED</b></dt>
<dt>0x00000004L</dt>
</dl>
</td>
<td width="60%">
The SID is enabled for access checks. When the system performs an access check, it checks for access-allowed and access-denied <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs) that apply to the SID. 




A SID without this attribute is ignored during an access check unless the SE_GROUP_USE_FOR_DENY_ONLY attribute is set.

</td>
</tr>
<tr>
<td width="40%"><a id="SE_GROUP_ENABLED_BY_DEFAULT"></a><a id="se_group_enabled_by_default"></a><dl>
<dt><b>SE_GROUP_ENABLED_BY_DEFAULT</b></dt>
<dt>0x00000002L</dt>
</dl>
</td>
<td width="60%">
The SID is enabled by default.

</td>
</tr>
<tr>
<td width="40%"><a id="SE_GROUP_INTEGRITY"></a><a id="se_group_integrity"></a><dl>
<dt><b>SE_GROUP_INTEGRITY</b></dt>
<dt>0x00000020L</dt>
</dl>
</td>
<td width="60%">
The SID is a mandatory integrity SID.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SE_GROUP_INTEGRITY_ENABLED"></a><a id="se_group_integrity_enabled"></a><dl>
<dt><b>SE_GROUP_INTEGRITY_ENABLED</b></dt>
<dt>0x00000040L</dt>
</dl>
</td>
<td width="60%">
The mandatory integrity SID is evaluated during access check.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SE_GROUP_LOGON_ID"></a><a id="se_group_logon_id"></a><dl>
<dt><b>SE_GROUP_LOGON_ID</b></dt>
<dt>0xC0000000L</dt>
</dl>
</td>
<td width="60%">
The SID is a logon SID that identifies the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a> associated with an access token.

</td>
</tr>
<tr>
<td width="40%"><a id="SE_GROUP_MANDATORY"></a><a id="se_group_mandatory"></a><dl>
<dt><b>SE_GROUP_MANDATORY</b></dt>
<dt>0x00000001L</dt>
</dl>
</td>
<td width="60%">
The SID cannot have the SE_GROUP_ENABLED attribute cleared by a call to the 
<a href="https://msdn.microsoft.com/839c4b58-4c61-4f72-8337-1e3dfa267ee5">AdjustTokenGroups</a> function. However, you can use the 
<a href="https://msdn.microsoft.com/e087f360-5d1d-4846-b3d6-214a426e5222">CreateRestrictedToken</a> function to convert a mandatory SID to a deny-only SID.

</td>
</tr>
<tr>
<td width="40%"><a id="SE_GROUP_OWNER"></a><a id="se_group_owner"></a><dl>
<dt><b>SE_GROUP_OWNER</b></dt>
<dt>0x00000008L</dt>
</dl>
</td>
<td width="60%">
The SID identifies a group account for which the user of the token is the owner of the group, or the SID can be assigned as the owner of the token or objects.

</td>
</tr>
<tr>
<td width="40%"><a id="SE_GROUP_RESOURCE"></a><a id="se_group_resource"></a><dl>
<dt><b>SE_GROUP_RESOURCE</b></dt>
<dt>0x20000000L</dt>
</dl>
</td>
<td width="60%">
The SID identifies a domain-local group.

</td>
</tr>
<tr>
<td width="40%"><a id="SE_GROUP_USE_FOR_DENY_ONLY"></a><a id="se_group_use_for_deny_only"></a><dl>
<dt><b>SE_GROUP_USE_FOR_DENY_ONLY</b></dt>
<dt>0x00000010L</dt>
</dl>
</td>
<td width="60%">
The SID is a deny-only SID in a 
<a href="https://msdn.microsoft.com/06580ab9-ff58-4aa9-bf88-9536a2e1981d">restricted token</a>. When the system performs an access check, it checks for access-denied ACEs that apply to the SID; it ignores access-allowed ACEs for the SID. 




If this attribute is set,  SE_GROUP_ENABLED is not set, and the SID cannot be reenabled. 

</td>
</tr>
</table>
 


### -field RestrictedSidCount

Number of restricted SIDs.


### -field RestrictedSidLength

Length, in bytes, required to hold all of the restricted SIDs.


### -field RestrictedSids

A pointer to an array of 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556742">SID_AND_ATTRIBUTES</a> structures that contain a set of restricted SIDs and corresponding attributes. 




The <b>Attributes</b> members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556742">SID_AND_ATTRIBUTES</a> structures can have the same values as those listed for the preceding <b>Sids</b> member.


### -field PrivilegeCount

Number of privileges.


### -field PrivilegeLength

Length, in bytes, needed to hold the privilege array.


### -field Privileges

Array of privileges.


### -field AuthenticationId

<a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Locally unique identifier</a> (LUID) of the authenticator of the token.


## -see-also




<a href="https://msdn.microsoft.com/839c4b58-4c61-4f72-8337-1e3dfa267ee5">AdjustTokenGroups</a>



<a href="https://msdn.microsoft.com/e087f360-5d1d-4846-b3d6-214a426e5222">CreateRestrictedToken</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556742">SID_AND_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556827">TOKEN_CONTROL</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556831">TOKEN_DEFAULT_DACL</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556838">TOKEN_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556842">TOKEN_OWNER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556845">TOKEN_PRIMARY_GROUP</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556846">TOKEN_PRIVILEGES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556848">TOKEN_SOURCE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556849">TOKEN_STATISTICS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556851">TOKEN_TYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556855">TOKEN_USER</a>
 

 

