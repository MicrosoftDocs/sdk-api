---
UID: NS:lmaccess._LOCALGROUP_MEMBERS_INFO_2
title: LOCALGROUP_MEMBERS_INFO_2
author: windows-sdk-content
description: The LOCALGROUP_MEMBERS_INFO_2 structure contains the security identifier (SID) and account information associated with a local group member.
old-location: netmgmt\localgroup_members_info_2_str.htm
tech.root: netmgmt
ms.assetid: f5cd6e84-1111-4558-bec4-26af13f21b61
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPLOCALGROUP_MEMBERS_INFO_2, *PLOCALGROUP_MEMBERS_INFO_2, LOCALGROUP_MEMBERS_INFO_2, LOCALGROUP_MEMBERS_INFO_2 structure [Network Management], LPLOCALGROUP_MEMBERS_INFO_2, LPLOCALGROUP_MEMBERS_INFO_2 structure pointer [Network Management], PLOCALGROUP_MEMBERS_INFO_2, PLOCALGROUP_MEMBERS_INFO_2 structure pointer [Network Management], SidTypeDeletedAccount, SidTypeGroup, SidTypeUnknown, SidTypeUser, SidTypeWellKnownGroup, _win32_localgroup_members_info_2_str, lmaccess/LOCALGROUP_MEMBERS_INFO_2, lmaccess/LPLOCALGROUP_MEMBERS_INFO_2, lmaccess/PLOCALGROUP_MEMBERS_INFO_2, netmgmt.localgroup_members_info_2_str"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - LOCALGROUP_MEMBERS_INFO_2
product: Windows
targetos: Windows
req.typenames: LOCALGROUP_MEMBERS_INFO_2, *PLOCALGROUP_MEMBERS_INFO_2, *LPLOCALGROUP_MEMBERS_INFO_2
req.redist: 
---

# LOCALGROUP_MEMBERS_INFO_2 structure


## -description


The 
				<b>LOCALGROUP_MEMBERS_INFO_2</b> structure contains the security identifier (SID) and account information associated with a local group member.


## -struct-fields




### -field lgrmi2_sid

Type: <b>PSID</b>

A pointer to a 
<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure that contains the security identifier (SID) of a local group member. The local group member can be a user account or a global group account.


### -field lgrmi2_sidusage

Type: <b>SID_NAME_USE</b>

The account type associated with the security identifier specified in the <b>lgrmi2_sid</b> member. The following values are valid. 



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
<a href="https://msdn.microsoft.com/eb2f95c4-9465-409b-b76c-9ccae1d05eda">Well-Known SIDs</a>.

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
 


### -field lgrmi2_domainandname

Type: <b>LPWSTR</b>

A pointer to the account name of the local group member identified by <b>lgrmi2_sid</b>. The <b>lgrmi2_domainandname</b> member includes the domain name and has the form: 




<pre class="syntax" xml:space="preserve"><code>&lt;DomainName&gt;\&lt;AccountName&gt;
</code></pre>

## -remarks



User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.




## -see-also




<a href="https://msdn.microsoft.com/e559cd90-942c-442a-b57f-7d2024523455">LOCALGROUP_MEMBERS_INFO_0</a>



<a href="https://msdn.microsoft.com/d6b1b729-cdd5-4ed3-a5a1-cf3a8b6cecf2">LOCALGROUP_MEMBERS_INFO_1</a>



<a href="https://msdn.microsoft.com/e8d1d884-c955-4706-bc3e-142469b02545">LOCALGROUP_MEMBERS_INFO_3
			</a>



<a href="https://msdn.microsoft.com/ed4c59d6-6532-4190-9807-95678053fc72">Local Group Functions</a>



<a href="https://msdn.microsoft.com/35770b32-dae9-46f5-84e3-1c31ca22f708">NetLocalGroupGetMembers</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

