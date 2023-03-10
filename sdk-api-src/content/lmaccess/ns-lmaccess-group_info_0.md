---
UID: NS:lmaccess._GROUP_INFO_0
title: GROUP_INFO_0 (lmaccess.h)
description: The GROUP_INFO_0 structure contains the name of a global group in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.
helpviewer_keywords: ["*LPGROUP_INFO_0","*PGROUP_INFO_0","GROUP_INFO_0","GROUP_INFO_0 structure [Network Management]","LPGROUP_INFO_0","LPGROUP_INFO_0 structure pointer [Network Management]","PGROUP_INFO_0","PGROUP_INFO_0 structure pointer [Network Management]","_win32_group_info_0_str","lmaccess/GROUP_INFO_0","lmaccess/LPGROUP_INFO_0","lmaccess/PGROUP_INFO_0","netmgmt.group_info_0_str"]
old-location: netmgmt\group_info_0_str.htm
tech.root: NetMgmt
ms.assetid: 019796d1-b987-45d2-90df-1d3b484217a9
ms.date: 12/05/2018
ms.keywords: '*LPGROUP_INFO_0, *PGROUP_INFO_0, GROUP_INFO_0, GROUP_INFO_0 structure [Network Management], LPGROUP_INFO_0, LPGROUP_INFO_0 structure pointer [Network Management], PGROUP_INFO_0, PGROUP_INFO_0 structure pointer [Network Management], _win32_group_info_0_str, lmaccess/GROUP_INFO_0, lmaccess/LPGROUP_INFO_0, lmaccess/PGROUP_INFO_0, netmgmt.group_info_0_str'
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
req.typenames: GROUP_INFO_0, *PGROUP_INFO_0, *LPGROUP_INFO_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GROUP_INFO_0
 - lmaccess/_GROUP_INFO_0
 - PGROUP_INFO_0
 - lmaccess/PGROUP_INFO_0
 - GROUP_INFO_0
 - lmaccess/GROUP_INFO_0
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
 - GROUP_INFO_0
---

# GROUP_INFO_0 structure


## -description

The
				<b>GROUP_INFO_0</b> structure contains the name of a global group in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.

## -struct-fields

### -field grpi0_name

Pointer to a null-terminated Unicode character string that specifies the name of the global group. For more information, see the following Remarks section. 




When you call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupsetinfo">NetGroupSetInfo</a> function this member specifies the new name of the global group.

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