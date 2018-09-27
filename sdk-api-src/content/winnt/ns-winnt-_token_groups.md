---
UID: NS:winnt._TOKEN_GROUPS
title: "_TOKEN_GROUPS"
author: windows-sdk-content
description: Contains information about the group security identifiers (SIDs) in an access token.
old-location: security\token_groups.htm
tech.root: secauthz
ms.assetid: 387dd7f8-4177-40fa-b5fd-bb4b371a0e64
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*PTOKEN_GROUPS, PTOKEN_GROUPS, PTOKEN_GROUPS structure pointer [Security], SE_GROUP_ENABLED, SE_GROUP_ENABLED_BY_DEFAULT, SE_GROUP_INTEGRITY, SE_GROUP_INTEGRITY_ENABLED, SE_GROUP_LOGON_ID, SE_GROUP_MANDATORY, SE_GROUP_OWNER, SE_GROUP_RESOURCE, SE_GROUP_USE_FOR_DENY_ONLY, TOKEN_GROUPS, TOKEN_GROUPS structure [Security], _TOKEN_GROUPS, _win32_token_groups_str, security.token_groups, winnt/PTOKEN_GROUPS, winnt/TOKEN_GROUPS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - TOKEN_GROUPS
product: Windows
targetos: Windows
req.typenames: TOKEN_GROUPS, *PTOKEN_GROUPS
req.redist: 
---

# _TOKEN_GROUPS structure


## -description


The <b>TOKEN_GROUPS</b> structure contains information about the group <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs) in an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a>.


## -struct-fields




### -field GroupCount

Specifies the number of groups in the access token. 


### -field Groups.size_is

 


### -field Groups.size_is.GroupCount

 


### -field Groups

Specifies an array of 
<a href="https://msdn.microsoft.com/d15d5a3f-6b38-4b92-b59c-ff0d27d111d9">SID_AND_ATTRIBUTES</a> structures that contain a set of SIDs and corresponding attributes. 




The <b>Attributes</b> members of the <a href="https://msdn.microsoft.com/d15d5a3f-6b38-4b92-b59c-ff0d27d111d9">SID_AND_ATTRIBUTES</a> structures can have the following values.

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

</td>
</tr>
<tr>
<td width="40%"><a id="SE_GROUP_INTEGRITY_ENABLED"></a><a id="se_group_integrity_enabled"></a><dl>
<dt><b>SE_GROUP_INTEGRITY_ENABLED</b></dt>
<dt>0x00000040L</dt>
</dl>
</td>
<td width="60%">
The SID is enabled for mandatory integrity checks.

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




If this attribute is set, SE_GROUP_ENABLED is not set, and the SID cannot be reenabled.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/839c4b58-4c61-4f72-8337-1e3dfa267ee5">AdjustTokenGroups</a>



<a href="https://msdn.microsoft.com/e087f360-5d1d-4846-b3d6-214a426e5222">CreateRestrictedToken</a>



<a href="https://msdn.microsoft.com/d15d5a3f-6b38-4b92-b59c-ff0d27d111d9">SID_AND_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/b87c942b-8e58-471d-8cdf-e46cdac647c4">TOKEN_CONTROL</a>



<a href="https://msdn.microsoft.com/29fb738f-1ecd-4b72-9aea-64698cd74c12">TOKEN_DEFAULT_DACL</a>



<a href="https://msdn.microsoft.com/cb606665-1266-4e71-a145-9b04bf157cdc">TOKEN_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/85617d56-ad46-40a3-a335-121f3c8edcc3">TOKEN_OWNER</a>



<a href="https://msdn.microsoft.com/d23ebe6c-36a3-434a-a0fa-fcdf50dd19a0">TOKEN_PRIMARY_GROUP</a>



<a href="https://msdn.microsoft.com/c9016511-740f-44f3-92ed-17cc518c6612">TOKEN_PRIVILEGES</a>



<a href="https://msdn.microsoft.com/9c533327-e4a0-4852-828c-622d190b7d1e">TOKEN_SOURCE</a>



<a href="https://msdn.microsoft.com/7fcc4a46-1bac-49c1-a239-b466d3bf31d9">TOKEN_STATISTICS</a>



<a href="https://msdn.microsoft.com/51b6717e-3fda-4af4-8995-4ac571eae2fd">TOKEN_TYPE</a>



<a href="https://msdn.microsoft.com/5dd8172d-7b1a-4cc0-b667-5fe91d278393">TOKEN_USER</a>
 

 

