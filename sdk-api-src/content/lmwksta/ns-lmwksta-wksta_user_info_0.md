---
UID: NS:lmwksta._WKSTA_USER_INFO_0
title: WKSTA_USER_INFO_0 (lmwksta.h)
description: The WKSTA_USER_INFO_0 structure contains the name of the user on a specified workstation.
helpviewer_keywords: ["*LPWKSTA_USER_INFO_0","*PWKSTA_USER_INFO_0","LPWKSTA_USER_INFO_0","LPWKSTA_USER_INFO_0 structure pointer [Network Management]","PWKSTA_USER_INFO_0","PWKSTA_USER_INFO_0 structure pointer [Network Management]","WKSTA_USER_INFO_0","WKSTA_USER_INFO_0 structure [Network Management]","_win32_wksta_user_info_0_str","lmwksta/LPWKSTA_USER_INFO_0","lmwksta/PWKSTA_USER_INFO_0","lmwksta/WKSTA_USER_INFO_0","netmgmt.wksta_user_info_0_str"]
old-location: netmgmt\wksta_user_info_0_str.htm
tech.root: NetMgmt
ms.assetid: 8bd8d8c7-4558-46cb-ab46-a2197d53e9f7
ms.date: 12/05/2018
ms.keywords: '*LPWKSTA_USER_INFO_0, *PWKSTA_USER_INFO_0, LPWKSTA_USER_INFO_0, LPWKSTA_USER_INFO_0 structure pointer [Network Management], PWKSTA_USER_INFO_0, PWKSTA_USER_INFO_0 structure pointer [Network Management], WKSTA_USER_INFO_0, WKSTA_USER_INFO_0 structure [Network Management], _win32_wksta_user_info_0_str, lmwksta/LPWKSTA_USER_INFO_0, lmwksta/PWKSTA_USER_INFO_0, lmwksta/WKSTA_USER_INFO_0, netmgmt.wksta_user_info_0_str'
req.header: lmwksta.h
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
req.typenames: WKSTA_USER_INFO_0, *PWKSTA_USER_INFO_0, *LPWKSTA_USER_INFO_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WKSTA_USER_INFO_0
 - lmwksta/_WKSTA_USER_INFO_0
 - PWKSTA_USER_INFO_0
 - lmwksta/PWKSTA_USER_INFO_0
 - WKSTA_USER_INFO_0
 - lmwksta/WKSTA_USER_INFO_0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmwksta.h
api_name:
 - WKSTA_USER_INFO_0
---

# WKSTA_USER_INFO_0 structure


## -description

The
				<b>WKSTA_USER_INFO_0</b> structure contains the name of the user on a specified workstation.

## -struct-fields

### -field wkui0_username

Specifies the name of the user currently logged on to the workstation.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

## -see-also

<a href="/windows/desktop/api/lmwksta/nf-lmwksta-netwkstauserenum">NetWkstaUserEnum</a>



<a href="/windows/desktop/api/lmwksta/nf-lmwksta-netwkstausergetinfo">NetWkstaUserGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/workstation-and-workstation-user-functions">Workstation and Workstation User Functions</a>