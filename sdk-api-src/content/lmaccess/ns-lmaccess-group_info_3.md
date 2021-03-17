---
UID: NS:lmaccess._GROUP_INFO_3
title: GROUP_INFO_3 (lmaccess.h)
description: The GROUP_INFO_3 structure contains information about a global group, including name, security identifier (SID), and resource attributes.
helpviewer_keywords: ["*PGROUP_INFO_3","GROUP_INFO_3","GROUP_INFO_3 structure [Network Management]","PGROUP_INFO_3","PGROUP_INFO_3 structure pointer [Network Management]","_win32_group_info_3_str","lmaccess/GROUP_INFO_3","lmaccess/PGROUP_INFO_3","netmgmt.group_info_3_str"]
old-location: netmgmt\group_info_3_str.htm
tech.root: NetMgmt
ms.assetid: aa0c3b6e-ab27-48b9-a37f-5cceb63c70fd
ms.date: 12/05/2018
ms.keywords: '*PGROUP_INFO_3, GROUP_INFO_3, GROUP_INFO_3 structure [Network Management], PGROUP_INFO_3, PGROUP_INFO_3 structure pointer [Network Management], _win32_group_info_3_str, lmaccess/GROUP_INFO_3, lmaccess/PGROUP_INFO_3, netmgmt.group_info_3_str'
req.header: lmaccess.h
req.include-header: Lm.h
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
req.typenames: GROUP_INFO_3, *PGROUP_INFO_3
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GROUP_INFO_3
 - lmaccess/_GROUP_INFO_3
 - PGROUP_INFO_3
 - lmaccess/PGROUP_INFO_3
 - GROUP_INFO_3
 - lmaccess/GROUP_INFO_3
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
 - GROUP_INFO_3
---

# GROUP_INFO_3 structure


## -description

The
				<b>GROUP_INFO_3</b> structure contains information about a global group, including name, security identifier (SID), and resource attributes.

## -struct-fields

### -field grpi3_name

Pointer to a null-terminated Unicode character string that specifies the name of the global group. 




When you call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupsetinfo">NetGroupSetInfo</a> function this member is ignored.

### -field grpi3_comment

Pointer to a null-terminated Unicode character string that contains a remark associated with the global group. This member can be a null string. The comment can contain MAXCOMMENTSZ characters.

### -field grpi3_group_sid

Pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure that contains the 
<a href="/windows/desktop/SecAuthZ/security-identifiers">security identifier (SID)</a> that uniquely identifies the global group. The 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> and 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> functions ignore this member.

### -field grpi3_attributes

These attributes are hard-coded to SE_GROUP_MANDATORY, SE_GROUP_ENABLED, and SE_GROUP_ENABLED_BY_DEFAULT. For more information, see 
<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>.

## -see-also

<a href="/windows/desktop/NetMgmt/group-functions">Group Functions</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupadd">NetGroupAdd</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupenum">NetGroupEnum</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupgetinfo">NetGroupGetInfo</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupsetinfo">NetGroupSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>