---
UID: NS:lmaccess._LOCALGROUP_MEMBERS_INFO_1
title: LOCALGROUP_MEMBERS_INFO_1 (lmaccess.h)
description: The LOCALGROUP_MEMBERS_INFO_1 structure contains the security identifier (SID) and account information associated with the member of a local group.
helpviewer_keywords: ["*LPLOCALGROUP_MEMBERS_INFO_1","*PLOCALGROUP_MEMBERS_INFO_1","LOCALGROUP_MEMBERS_INFO_1","LOCALGROUP_MEMBERS_INFO_1 structure [Network Management]","LPLOCALGROUP_MEMBERS_INFO_1","LPLOCALGROUP_MEMBERS_INFO_1 structure pointer [Network Management]","PLOCALGROUP_MEMBERS_INFO_1","PLOCALGROUP_MEMBERS_INFO_1 structure pointer [Network Management]","SidTypeDeletedAccount","SidTypeGroup","SidTypeUnknown","SidTypeUser","SidTypeWellKnownGroup","_win32_localgroup_members_info_1_str","lmaccess/LOCALGROUP_MEMBERS_INFO_1","lmaccess/LPLOCALGROUP_MEMBERS_INFO_1","lmaccess/PLOCALGROUP_MEMBERS_INFO_1","netmgmt.localgroup_members_info_1_str"]
old-location: netmgmt\localgroup_members_info_1_str.htm
tech.root: NetMgmt
ms.assetid: d6b1b729-cdd5-4ed3-a5a1-cf3a8b6cecf2
ms.date: 12/05/2018
ms.keywords: '*LPLOCALGROUP_MEMBERS_INFO_1, *PLOCALGROUP_MEMBERS_INFO_1, LOCALGROUP_MEMBERS_INFO_1, LOCALGROUP_MEMBERS_INFO_1 structure [Network Management], LPLOCALGROUP_MEMBERS_INFO_1, LPLOCALGROUP_MEMBERS_INFO_1 structure pointer [Network Management], PLOCALGROUP_MEMBERS_INFO_1, PLOCALGROUP_MEMBERS_INFO_1 structure pointer [Network Management], SidTypeDeletedAccount, SidTypeGroup, SidTypeUnknown, SidTypeUser, SidTypeWellKnownGroup, _win32_localgroup_members_info_1_str, lmaccess/LOCALGROUP_MEMBERS_INFO_1, lmaccess/LPLOCALGROUP_MEMBERS_INFO_1, lmaccess/PLOCALGROUP_MEMBERS_INFO_1, netmgmt.localgroup_members_info_1_str'
req.header: lmaccess.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: LOCALGROUP_MEMBERS_INFO_1, *PLOCALGROUP_MEMBERS_INFO_1, *LPLOCALGROUP_MEMBERS_INFO_1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LOCALGROUP_MEMBERS_INFO_1
 - lmaccess/_LOCALGROUP_MEMBERS_INFO_1
 - PLOCALGROUP_MEMBERS_INFO_1
 - lmaccess/PLOCALGROUP_MEMBERS_INFO_1
 - LOCALGROUP_MEMBERS_INFO_1
 - lmaccess/LOCALGROUP_MEMBERS_INFO_1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - LOCALGROUP_MEMBERS_INFO_1
---

# LOCALGROUP_MEMBERS_INFO_1 structure


## -description

The 
				<b>LOCALGROUP_MEMBERS_INFO_1</b> structure contains the security identifier (SID) and account information associated with the member of a local group.

## -struct-fields

### -field lgrmi1_sid

Type: <b>PSID</b>

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure that contains the security identifier (SID) of an account that is a member of this local group member. The account can be a user account or a global group account.

### -field lgrmi1_sidusage

Type: <b>SID_NAME_USE</b>

The account type associated with the security identifier specified in the <b>lgrmi1_sid</b>  member. The following values are valid. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SidTypeUser"></a><a id="sidtypeuser"></a><a id="SIDTYPEUSER"></a><dl>
<dt><b>SidTypeUser</b></dt>
</dl>
</td>
<td width="60%">
The account is a user account.

</td>
</tr>
<tr>
<td width="40%"><a id="SidTypeGroup"></a><a id="sidtypegroup"></a><a id="SIDTYPEGROUP"></a><dl>
<dt><b>SidTypeGroup</b></dt>
</dl>
</td>
<td width="60%">
The account is a global group account.

</td>
</tr>
<tr>
<td width="40%"><a id="SidTypeWellKnownGroup"></a><a id="sidtypewellknowngroup"></a><a id="SIDTYPEWELLKNOWNGROUP"></a><dl>
<dt><b>SidTypeWellKnownGroup</b></dt>
</dl>
</td>
<td width="60%">
The account is a well-known group account (such as Everyone). For more information, see 
<a href="/windows/desktop/SecAuthZ/well-known-sids">Well-Known SIDs</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SidTypeDeletedAccount"></a><a id="sidtypedeletedaccount"></a><a id="SIDTYPEDELETEDACCOUNT"></a><dl>
<dt><b>SidTypeDeletedAccount</b></dt>
</dl>
</td>
<td width="60%">
The account has been deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="SidTypeUnknown"></a><a id="sidtypeunknown"></a><a id="SIDTYPEUNKNOWN"></a><dl>
<dt><b>SidTypeUnknown</b></dt>
</dl>
</td>
<td width="60%">
The account type cannot be determined.

</td>
</tr>
</table>

### -field lgrmi1_name

Type: <b>LPWSTR</b>

A pointer to the account name of the local group member identified by the <b>lgrmi1_sid</b> member. The <b>lgrmi1_name</b> member does not include the domain name. For more information, see the following Remarks section.

## -remarks

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

## -see-also

<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_members_info_0">LOCALGROUP_MEMBERS_INFO_0</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_members_info_2">LOCALGROUP_MEMBERS_INFO_2</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_members_info_3">LOCALGROUP_MEMBERS_INFO_3</a>



<a href="/windows/desktop/NetMgmt/local-group-functions">Local Group Functions</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupgetmembers">NetLocalGroupGetMembers</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>