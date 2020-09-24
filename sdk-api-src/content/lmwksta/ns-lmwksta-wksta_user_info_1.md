---
UID: NS:lmwksta._WKSTA_USER_INFO_1
title: WKSTA_USER_INFO_1 (lmwksta.h)
description: The WKSTA_USER_INFO_1 structure contains user information as it pertains to a specific workstation. The information includes the name of the current user and the domains accessed by the workstation.
helpviewer_keywords: ["*LPWKSTA_USER_INFO_1","*PWKSTA_USER_INFO_1","LPWKSTA_USER_INFO_1","LPWKSTA_USER_INFO_1 structure pointer [Network Management]","PWKSTA_USER_INFO_1","PWKSTA_USER_INFO_1 structure pointer [Network Management]","WKSTA_USER_INFO_1","WKSTA_USER_INFO_1 structure [Network Management]","_win32_wksta_user_info_1_str","lmwksta/LPWKSTA_USER_INFO_1","lmwksta/PWKSTA_USER_INFO_1","lmwksta/WKSTA_USER_INFO_1","netmgmt.wksta_user_info_1_str"]
old-location: netmgmt\wksta_user_info_1_str.htm
tech.root: NetMgmt
ms.assetid: a30747de-6cb0-41dc-95a7-be3d471056d5
ms.date: 12/05/2018
ms.keywords: '*LPWKSTA_USER_INFO_1, *PWKSTA_USER_INFO_1, LPWKSTA_USER_INFO_1, LPWKSTA_USER_INFO_1 structure pointer [Network Management], PWKSTA_USER_INFO_1, PWKSTA_USER_INFO_1 structure pointer [Network Management], WKSTA_USER_INFO_1, WKSTA_USER_INFO_1 structure [Network Management], _win32_wksta_user_info_1_str, lmwksta/LPWKSTA_USER_INFO_1, lmwksta/PWKSTA_USER_INFO_1, lmwksta/WKSTA_USER_INFO_1, netmgmt.wksta_user_info_1_str'
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
req.typenames: WKSTA_USER_INFO_1, *PWKSTA_USER_INFO_1, *LPWKSTA_USER_INFO_1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WKSTA_USER_INFO_1
 - lmwksta/_WKSTA_USER_INFO_1
 - PWKSTA_USER_INFO_1
 - lmwksta/PWKSTA_USER_INFO_1
 - WKSTA_USER_INFO_1
 - lmwksta/WKSTA_USER_INFO_1
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
 - WKSTA_USER_INFO_1
---

# WKSTA_USER_INFO_1 structure


## -description

The
				<b>WKSTA_USER_INFO_1</b> structure contains user information as it pertains to a specific workstation. The information includes the name of the current user and the domains accessed by the workstation.

## -struct-fields

### -field wkui1_username

Specifies the name of the user currently logged on to the workstation.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

### -field wkui1_logon_domain

Specifies the name of the domain in which the user is currently logged on.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

### -field wkui1_oth_domains

Specifies the list of operating system domains browsed by the workstation. The domain names are separated by blanks.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

### -field wkui1_logon_server

Specifies the name of the server that authenticated the user.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

## -see-also

<a href="/windows/desktop/api/lmwksta/nf-lmwksta-netwkstauserenum">NetWkstaUserEnum</a>



<a href="/windows/desktop/api/lmwksta/nf-lmwksta-netwkstausergetinfo">NetWkstaUserGetInfo</a>



<a href="/windows/desktop/api/lmwksta/nf-lmwksta-netwkstausersetinfo">NetWkstaUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/workstation-and-workstation-user-functions">Workstation and Workstation User Functions</a>