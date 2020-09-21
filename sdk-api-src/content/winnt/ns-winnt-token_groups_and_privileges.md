---
UID: NS:winnt._TOKEN_GROUPS_AND_PRIVILEGES
title: TOKEN_GROUPS_AND_PRIVILEGES (winnt.h)
description: Contains information about the group security identifiers (SIDs) and privileges in an access token.
helpviewer_keywords: ["*PTOKEN_GROUPS_AND_PRIVILEGES","PTOKEN_GROUPS_AND_PRIVILEGES","PTOKEN_GROUPS_AND_PRIVILEGES structure pointer [Security]","SE_GROUP_ENABLED","SE_GROUP_ENABLED_BY_DEFAULT","SE_GROUP_INTEGRITY","SE_GROUP_INTEGRITY_ENABLED","SE_GROUP_LOGON_ID","SE_GROUP_MANDATORY","SE_GROUP_OWNER","SE_GROUP_RESOURCE","SE_GROUP_USE_FOR_DENY_ONLY","TOKEN_GROUPS_AND_PRIVILEGES","TOKEN_GROUPS_AND_PRIVILEGES structure [Security]","_TOKEN_GROUPS_AND_PRIVILEGES","_win32_token_groups_and_privileges","security.token_groups_and_privileges","winnt/PTOKEN_GROUPS_AND_PRIVILEGES","winnt/TOKEN_GROUPS_AND_PRIVILEGES"]
old-location: security\token_groups_and_privileges.htm
tech.root: security
ms.assetid: 085ccd0a-d6c2-48ca-ad2a-933f22831b14
ms.date: 12/05/2018
ms.keywords: '*PTOKEN_GROUPS_AND_PRIVILEGES, PTOKEN_GROUPS_AND_PRIVILEGES, PTOKEN_GROUPS_AND_PRIVILEGES structure pointer [Security], SE_GROUP_ENABLED, SE_GROUP_ENABLED_BY_DEFAULT, SE_GROUP_INTEGRITY, SE_GROUP_INTEGRITY_ENABLED, SE_GROUP_LOGON_ID, SE_GROUP_MANDATORY, SE_GROUP_OWNER, SE_GROUP_RESOURCE, SE_GROUP_USE_FOR_DENY_ONLY, TOKEN_GROUPS_AND_PRIVILEGES, TOKEN_GROUPS_AND_PRIVILEGES structure [Security], _TOKEN_GROUPS_AND_PRIVILEGES, _win32_token_groups_and_privileges, security.token_groups_and_privileges, winnt/PTOKEN_GROUPS_AND_PRIVILEGES, winnt/TOKEN_GROUPS_AND_PRIVILEGES'
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
targetos: Windows
req.typenames: TOKEN_GROUPS_AND_PRIVILEGES, *PTOKEN_GROUPS_AND_PRIVILEGES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TOKEN_GROUPS_AND_PRIVILEGES
 - winnt/_TOKEN_GROUPS_AND_PRIVILEGES
 - PTOKEN_GROUPS_AND_PRIVILEGES
 - winnt/PTOKEN_GROUPS_AND_PRIVILEGES
 - TOKEN_GROUPS_AND_PRIVILEGES
 - winnt/TOKEN_GROUPS_AND_PRIVILEGES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - TOKEN_GROUPS_AND_PRIVILEGES
---

# TOKEN_GROUPS_AND_PRIVILEGES structure


## -description

The <b>TOKEN_GROUPS_AND_PRIVILEGES</b> structure contains information about the group <a href="/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs) and privileges in an <a href="/windows/desktop/SecGloss/a-gly">access token</a>.

## -struct-fields

### -field SidCount

Number of SIDs in the access token.

### -field SidLength

Length, in bytes, required to hold all of the user SIDs and the account SID for the group.

### -field Sids

A pointer to an array of 
<a href="/windows/desktop/api/winnt/ns-winnt-sid_and_attributes">SID_AND_ATTRIBUTES</a> structures that contain a set of SIDs and corresponding attributes.

The <b>Attributes</b> members of the <a href="/windows/desktop/api/winnt/ns-winnt-sid_and_attributes">SID_AND_ATTRIBUTES</a> structures can have the following values.

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
The SID is enabled for access checks. When the system performs an access check, it checks for access-allowed and access-denied <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs) that apply to the SID. 




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
The SID is a logon SID that identifies the <a href="/windows/desktop/SecGloss/l-gly">logon session</a> associated with an access token.

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
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups">AdjustTokenGroups</a> function. However, you can use the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken">CreateRestrictedToken</a> function to convert a mandatory SID to a deny-only SID.

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
<a href="/windows/desktop/SecAuthZ/restricted-tokens">restricted token</a>. When the system performs an access check, it checks for access-denied ACEs that apply to the SID; it ignores access-allowed ACEs for the SID. 




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
<a href="/windows/desktop/api/winnt/ns-winnt-sid_and_attributes">SID_AND_ATTRIBUTES</a> structures that contain a set of restricted SIDs and corresponding attributes. 




The <b>Attributes</b> members of the <a href="/windows/desktop/api/winnt/ns-winnt-sid_and_attributes">SID_AND_ATTRIBUTES</a> structures can have the same values as those listed for the preceding <b>Sids</b> member.

### -field PrivilegeCount

Number of privileges.

### -field PrivilegeLength

Length, in bytes, needed to hold the privilege array.

### -field Privileges

Array of privileges.

### -field AuthenticationId

<a href="/windows/desktop/SecGloss/l-gly">Locally unique identifier</a> (LUID) of the authenticator of the token.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups">AdjustTokenGroups</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken">CreateRestrictedToken</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid_and_attributes">SID_AND_ATTRIBUTES</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_control">TOKEN_CONTROL</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_default_dacl">TOKEN_DEFAULT_DACL</a>



<a href="/windows/desktop/api/winnt/ne-winnt-token_information_class">TOKEN_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_owner">TOKEN_OWNER</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_primary_group">TOKEN_PRIMARY_GROUP</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_source">TOKEN_SOURCE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_statistics">TOKEN_STATISTICS</a>



<a href="/windows/desktop/api/winnt/ne-winnt-token_type">TOKEN_TYPE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_user">TOKEN_USER</a>