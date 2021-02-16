---
UID: NS:lmaccess._LOCALGROUP_USERS_INFO_0
title: LOCALGROUP_USERS_INFO_0 (lmaccess.h)
description: The LOCALGROUP_USERS_INFO_0 structure contains local group member information.
helpviewer_keywords: ["*LPLOCALGROUP_USERS_INFO_0","*PLOCALGROUP_USERS_INFO_0","LOCALGROUP_USERS_INFO_0","LOCALGROUP_USERS_INFO_0 structure [Network Management]","LPLOCALGROUP_USERS_INFO_0","LPLOCALGROUP_USERS_INFO_0 structure pointer [Network Management]","PLOCALGROUP_USERS_INFO_0","PLOCALGROUP_USERS_INFO_0 structure pointer [Network Management]","_win32_localgroup_users_info_0_str","lmaccess/LOCALGROUP_USERS_INFO_0","lmaccess/LPLOCALGROUP_USERS_INFO_0","lmaccess/PLOCALGROUP_USERS_INFO_0","netmgmt.localgroup_users_info_0_str"]
old-location: netmgmt\localgroup_users_info_0_str.htm
tech.root: NetMgmt
ms.assetid: e9358f19-ec8f-4454-896c-c9fadb848378
ms.date: 12/05/2018
ms.keywords: '*LPLOCALGROUP_USERS_INFO_0, *PLOCALGROUP_USERS_INFO_0, LOCALGROUP_USERS_INFO_0, LOCALGROUP_USERS_INFO_0 structure [Network Management], LPLOCALGROUP_USERS_INFO_0, LPLOCALGROUP_USERS_INFO_0 structure pointer [Network Management], PLOCALGROUP_USERS_INFO_0, PLOCALGROUP_USERS_INFO_0 structure pointer [Network Management], _win32_localgroup_users_info_0_str, lmaccess/LOCALGROUP_USERS_INFO_0, lmaccess/LPLOCALGROUP_USERS_INFO_0, lmaccess/PLOCALGROUP_USERS_INFO_0, netmgmt.localgroup_users_info_0_str'
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
req.typenames: LOCALGROUP_USERS_INFO_0, *PLOCALGROUP_USERS_INFO_0, *LPLOCALGROUP_USERS_INFO_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LOCALGROUP_USERS_INFO_0
 - lmaccess/_LOCALGROUP_USERS_INFO_0
 - PLOCALGROUP_USERS_INFO_0
 - lmaccess/PLOCALGROUP_USERS_INFO_0
 - LOCALGROUP_USERS_INFO_0
 - lmaccess/LOCALGROUP_USERS_INFO_0
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
 - LOCALGROUP_USERS_INFO_0
---

# LOCALGROUP_USERS_INFO_0 structure


## -description

The 
				<b>LOCALGROUP_USERS_INFO_0</b> structure contains local group member information.

## -struct-fields

### -field lgrui0_name

Pointer to a Unicode string specifying the name of a local group to which the user belongs.

## -remarks

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

## -see-also

<a href="/windows/desktop/NetMgmt/local-group-functions">Local Group Functions</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetlocalgroups">NetUserGetLocalGroups</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>