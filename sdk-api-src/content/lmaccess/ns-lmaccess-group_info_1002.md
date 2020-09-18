---
UID: NS:lmaccess._GROUP_INFO_1002
title: GROUP_INFO_1002 (lmaccess.h)
description: The GROUP_INFO_1002 structure contains a comment to associate with a global group.
helpviewer_keywords: ["*LPGROUP_INFO_1002","*PGROUP_INFO_1002","GROUP_INFO_1002","GROUP_INFO_1002 structure [Network Management]","LPGROUP_INFO_1002","LPGROUP_INFO_1002 structure pointer [Network Management]","PGROUP_INFO_1002","PGROUP_INFO_1002 structure pointer [Network Management]","_win32_group_info_1002_str","lmaccess/GROUP_INFO_1002","lmaccess/LPGROUP_INFO_1002","lmaccess/PGROUP_INFO_1002","netmgmt.group_info_1002_str"]
old-location: netmgmt\group_info_1002_str.htm
tech.root: NetMgmt
ms.assetid: 9c322ef5-4f98-44ad-8b57-40f8533eb9c1
ms.date: 12/05/2018
ms.keywords: '*LPGROUP_INFO_1002, *PGROUP_INFO_1002, GROUP_INFO_1002, GROUP_INFO_1002 structure [Network Management], LPGROUP_INFO_1002, LPGROUP_INFO_1002 structure pointer [Network Management], PGROUP_INFO_1002, PGROUP_INFO_1002 structure pointer [Network Management], _win32_group_info_1002_str, lmaccess/GROUP_INFO_1002, lmaccess/LPGROUP_INFO_1002, lmaccess/PGROUP_INFO_1002, netmgmt.group_info_1002_str'
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
req.typenames: GROUP_INFO_1002, *PGROUP_INFO_1002, *LPGROUP_INFO_1002
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GROUP_INFO_1002
 - lmaccess/_GROUP_INFO_1002
 - PGROUP_INFO_1002
 - lmaccess/PGROUP_INFO_1002
 - GROUP_INFO_1002
 - lmaccess/GROUP_INFO_1002
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
 - GROUP_INFO_1002
---

# GROUP_INFO_1002 structure


## -description

The
				<b>GROUP_INFO_1002</b> structure contains a comment to associate with a global group.

## -struct-fields

### -field grpi1002_comment

Pointer to a null-terminated Unicode character string that contains a remark to associate with the global group. This member can be a null string. The comment can contain MAXCOMMENTSZ characters.

## -see-also

<a href="/windows/desktop/NetMgmt/group-functions">Group Functions</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupsetinfo">NetGroupSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>