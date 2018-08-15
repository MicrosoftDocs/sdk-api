---
UID: NS:lmwksta._WKSTA_USER_INFO_1101
title: "_WKSTA_USER_INFO_1101"
author: windows-sdk-content
description: The WKSTA_USER_INFO_1101 structure contains information about the domains accessed by a workstation.
old-location: netmgmt\wksta_user_info_1101_str.htm
old-project: netmgmt
ms.assetid: 88772ba2-046b-4b03-ae02-d851075e4363
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPWKSTA_USER_INFO_1101, *PWKSTA_USER_INFO_1101, LPWKSTA_USER_INFO_1101, LPWKSTA_USER_INFO_1101 structure pointer [Network Management], PWKSTA_USER_INFO_1101, PWKSTA_USER_INFO_1101 structure pointer [Network Management], WKSTA_USER_INFO_1101, WKSTA_USER_INFO_1101 structure [Network Management], _WKSTA_USER_INFO_1101, _win32_wksta_user_info_1101_str, lmwksta/LPWKSTA_USER_INFO_1101, lmwksta/PWKSTA_USER_INFO_1101, lmwksta/WKSTA_USER_INFO_1101, netmgmt.wksta_user_info_1101_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lmwksta.h
req.include-header: Lm.h
req.redist: 
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
tech.root: 
req.typenames: WKSTA_USER_INFO_1101, *PWKSTA_USER_INFO_1101, *LPWKSTA_USER_INFO_1101
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmwksta.h
api_name:
 - WKSTA_USER_INFO_1101
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _WKSTA_USER_INFO_1101 structure


## -description


The
				<b>WKSTA_USER_INFO_1101</b> structure contains information about the domains accessed by a workstation.


## -struct-fields




### -field wkui1101_oth_domains

Specifies the list of operating system domains browsed by the workstation. The domain names are separated by blanks.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


## -see-also




<a href="https://msdn.microsoft.com/25ec7a49-fd26-4105-823b-a257a57f724e">NetWkstaUserGetInfo</a>



<a href="https://msdn.microsoft.com/d48667a3-5ae9-4a7d-9af6-14f08835940d">NetWkstaUserSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/cc400f43-297b-4ff4-8353-b268839c48b8">Workstation and Workstation User Functions</a>
 

 

