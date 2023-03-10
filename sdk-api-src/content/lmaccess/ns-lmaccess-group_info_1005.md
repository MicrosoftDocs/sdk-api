---
UID: NS:lmaccess._GROUP_INFO_1005
title: GROUP_INFO_1005 (lmaccess.h)
description: The GROUP_INFO_1005 structure contains the resource attributes associated with a global group.
helpviewer_keywords: ["*LPGROUP_INFO_1005","*PGROUP_INFO_1005","GROUP_INFO_1005","GROUP_INFO_1005 structure [Network Management]","LPGROUP_INFO_1005","LPGROUP_INFO_1005 structure pointer [Network Management]","PGROUP_INFO_1005","PGROUP_INFO_1005 structure pointer [Network Management]","_win32_group_info_1005_str","lmaccess/GROUP_INFO_1005","lmaccess/LPGROUP_INFO_1005","lmaccess/PGROUP_INFO_1005","netmgmt.group_info_1005_str"]
old-location: netmgmt\group_info_1005_str.htm
tech.root: NetMgmt
ms.assetid: bd93820a-e019-45f4-88c7-011a517955ad
ms.date: 12/05/2018
ms.keywords: '*LPGROUP_INFO_1005, *PGROUP_INFO_1005, GROUP_INFO_1005, GROUP_INFO_1005 structure [Network Management], LPGROUP_INFO_1005, LPGROUP_INFO_1005 structure pointer [Network Management], PGROUP_INFO_1005, PGROUP_INFO_1005 structure pointer [Network Management], _win32_group_info_1005_str, lmaccess/GROUP_INFO_1005, lmaccess/LPGROUP_INFO_1005, lmaccess/PGROUP_INFO_1005, netmgmt.group_info_1005_str'
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
req.typenames: GROUP_INFO_1005, *PGROUP_INFO_1005, *LPGROUP_INFO_1005
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GROUP_INFO_1005
 - lmaccess/_GROUP_INFO_1005
 - PGROUP_INFO_1005
 - lmaccess/PGROUP_INFO_1005
 - GROUP_INFO_1005
 - lmaccess/GROUP_INFO_1005
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
 - GROUP_INFO_1005
---

# GROUP_INFO_1005 structure


## -description

The
				<b>GROUP_INFO_1005</b> structure contains the resource attributes associated with a global group.

## -struct-fields

### -field grpi1005_attributes

These attributes are hard-coded to SE_GROUP_MANDATORY, SE_GROUP_ENABLED, and SE_GROUP_ENABLED_BY_DEFAULT. For more information, see 
<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>.

## -see-also

<a href="/windows/desktop/NetMgmt/group-functions">Group Functions</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupsetinfo">NetGroupSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>