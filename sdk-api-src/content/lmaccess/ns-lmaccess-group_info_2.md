---
UID: NS:lmaccess._GROUP_INFO_2
title: GROUP_INFO_2 (lmaccess.h)
description: The GROUP_INFO_2 structure contains information about a global group, including name, identifier, and resource attributes.
helpviewer_keywords: ["*PGROUP_INFO_2","GROUP_INFO_2","GROUP_INFO_2 structure [Network Management]","PGROUP_INFO_2","PGROUP_INFO_2 structure pointer [Network Management]","_win32_group_info_2_str","lmaccess/GROUP_INFO_2","lmaccess/PGROUP_INFO_2","netmgmt.group_info_2_str"]
old-location: netmgmt\group_info_2_str.htm
tech.root: NetMgmt
ms.assetid: 2c17a70c-7b62-4dcc-9dc6-2f4b8c41d6ec
ms.date: 12/05/2018
ms.keywords: '*PGROUP_INFO_2, GROUP_INFO_2, GROUP_INFO_2 structure [Network Management], PGROUP_INFO_2, PGROUP_INFO_2 structure pointer [Network Management], _win32_group_info_2_str, lmaccess/GROUP_INFO_2, lmaccess/PGROUP_INFO_2, netmgmt.group_info_2_str'
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
req.typenames: GROUP_INFO_2, *PGROUP_INFO_2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GROUP_INFO_2
 - lmaccess/_GROUP_INFO_2
 - PGROUP_INFO_2
 - lmaccess/PGROUP_INFO_2
 - GROUP_INFO_2
 - lmaccess/GROUP_INFO_2
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
 - GROUP_INFO_2
---

# GROUP_INFO_2 structure


## -description

The
				<b>GROUP_INFO_2</b> structure contains information about a global group, including name, identifier, and resource attributes.

It is recommended that you use the 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_info_3">GROUP_INFO_3</a> structure instead.

## -struct-fields

### -field grpi2_name

Pointer to a null-terminated Unicode character string that specifies the name of the global group. For more information, see the following Remarks section. 




When you call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupsetinfo">NetGroupSetInfo</a> function this member is ignored.

### -field grpi2_comment

Pointer to a null-terminated Unicode character string that contains a remark associated with the global group. This member can be a null string. The comment can contain MAXCOMMENTSZ characters.

### -field grpi2_group_id

The relative identifier (RID) of the global group. The 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> and 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> functions ignore this member. For more information about RIDs, see 
<a href="/windows/desktop/SecAuthZ/sid-components">SID Components</a>.

### -field grpi2_attributes

These attributes are hard-coded to SE_GROUP_MANDATORY, SE_GROUP_ENABLED, and SE_GROUP_ENABLED_BY_DEFAULT. For more information, see 
<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>.

## -remarks

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

## -see-also

<a href="/windows/desktop/NetMgmt/group-functions">Group Functions</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupadd">NetGroupAdd</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupenum">NetGroupEnum</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupgetinfo">NetGroupGetInfo</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupsetinfo">NetGroupSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>