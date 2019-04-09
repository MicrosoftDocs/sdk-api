---
UID: NS:lmwksta._WKSTA_USER_INFO_1
title: WKSTA_USER_INFO_1 (lmwksta.h)
author: windows-sdk-content
description: The WKSTA_USER_INFO_1 structure contains user information as it pertains to a specific workstation. The information includes the name of the current user and the domains accessed by the workstation.
old-location: netmgmt\wksta_user_info_1_str.htm
tech.root: NetMgmt
ms.assetid: a30747de-6cb0-41dc-95a7-be3d471056d5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPWKSTA_USER_INFO_1, *PWKSTA_USER_INFO_1, LPWKSTA_USER_INFO_1, LPWKSTA_USER_INFO_1 structure pointer [Network Management], PWKSTA_USER_INFO_1, PWKSTA_USER_INFO_1 structure pointer [Network Management], WKSTA_USER_INFO_1, WKSTA_USER_INFO_1 structure [Network Management], _win32_wksta_user_info_1_str, lmwksta/LPWKSTA_USER_INFO_1, lmwksta/PWKSTA_USER_INFO_1, lmwksta/WKSTA_USER_INFO_1, netmgmt.wksta_user_info_1_str"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmwksta.h
api_name:
 - WKSTA_USER_INFO_1
product: Windows
targetos: Windows
req.typenames: WKSTA_USER_INFO_1, *PWKSTA_USER_INFO_1, *LPWKSTA_USER_INFO_1
req.redist: 
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




<a href="https://msdn.microsoft.com/42eaeb70-3ce8-4eae-b20b-4729db90a7ef">NetWkstaUserEnum</a>



<a href="https://msdn.microsoft.com/25ec7a49-fd26-4105-823b-a257a57f724e">NetWkstaUserGetInfo</a>



<a href="https://msdn.microsoft.com/d48667a3-5ae9-4a7d-9af6-14f08835940d">NetWkstaUserSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/cc400f43-297b-4ff4-8353-b268839c48b8">Workstation and Workstation User Functions</a>
 

 

