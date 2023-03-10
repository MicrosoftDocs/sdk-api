---
UID: NS:lmaccess._GROUP_USERS_INFO_0
title: GROUP_USERS_INFO_0 (lmaccess.h)
description: The GROUP_USERS_INFO_0 structure contains global group member information.
helpviewer_keywords: ["*LPGROUP_USERS_INFO_0","*PGROUP_USERS_INFO_0","GROUP_USERS_INFO_0","GROUP_USERS_INFO_0 structure [Network Management]","LPGROUP_USERS_INFO_0","LPGROUP_USERS_INFO_0 structure pointer [Network Management]","PGROUP_USERS_INFO_0","PGROUP_USERS_INFO_0 structure pointer [Network Management]","_win32_group_users_info_0_str","lmaccess/GROUP_USERS_INFO_0","lmaccess/LPGROUP_USERS_INFO_0","lmaccess/PGROUP_USERS_INFO_0","netmgmt.group_users_info_0_str"]
old-location: netmgmt\group_users_info_0_str.htm
tech.root: NetMgmt
ms.assetid: cc0e5d27-91f1-4640-bb80-e73899fabba9
ms.date: 12/05/2018
ms.keywords: '*LPGROUP_USERS_INFO_0, *PGROUP_USERS_INFO_0, GROUP_USERS_INFO_0, GROUP_USERS_INFO_0 structure [Network Management], LPGROUP_USERS_INFO_0, LPGROUP_USERS_INFO_0 structure pointer [Network Management], PGROUP_USERS_INFO_0, PGROUP_USERS_INFO_0 structure pointer [Network Management], _win32_group_users_info_0_str, lmaccess/GROUP_USERS_INFO_0, lmaccess/LPGROUP_USERS_INFO_0, lmaccess/PGROUP_USERS_INFO_0, netmgmt.group_users_info_0_str'
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
req.typenames: GROUP_USERS_INFO_0, *PGROUP_USERS_INFO_0, *LPGROUP_USERS_INFO_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GROUP_USERS_INFO_0
 - lmaccess/_GROUP_USERS_INFO_0
 - PGROUP_USERS_INFO_0
 - lmaccess/PGROUP_USERS_INFO_0
 - GROUP_USERS_INFO_0
 - lmaccess/GROUP_USERS_INFO_0
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
 - GROUP_USERS_INFO_0
---

# GROUP_USERS_INFO_0 structure


## -description

The
				<b>GROUP_USERS_INFO_0</b> structure contains global group member information.

## -struct-fields

### -field grui0_name

A pointer to a null-terminated Unicode character string that specifies a name. For more information, see the Remarks section.

## -remarks

If you are calling the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupgetusers">NetGroupGetUsers</a> function or the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupsetusers">NetGroupSetUsers</a> function, the <b>grui0_name</b> member contains the name of a user that is a member of the specified group.

If you are calling the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetgroups">NetUserGetGroups</a> function or the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetgroups">NetUserSetGroups</a> function, the <b>grui0_name</b> member contains the name of a global group to which the specified user belongs. 

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

## -see-also

<a href="/windows/desktop/api/lmaccess/ns-lmaccess-group_users_info_1">GROUP_USERS_INFO_1</a>



<a href="/windows/desktop/NetMgmt/group-functions">Group Functions</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupgetusers">NetGroupGetUsers</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupsetusers">NetGroupSetUsers</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetgroups">NetUserGetGroups</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetinfo">NetUserGetInfo</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetgroups">NetUserSetGroups</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>