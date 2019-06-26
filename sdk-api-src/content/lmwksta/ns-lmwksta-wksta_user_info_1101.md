---
UID: NS:lmwksta._WKSTA_USER_INFO_1101
title: WKSTA_USER_INFO_1101 (lmwksta.h)
author: windows-sdk-content
description: The WKSTA_USER_INFO_1101 structure contains information about the domains accessed by a workstation.
old-location: netmgmt\wksta_user_info_1101_str.htm
tech.root: NetMgmt
ms.assetid: 88772ba2-046b-4b03-ae02-d851075e4363
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPWKSTA_USER_INFO_1101, *PWKSTA_USER_INFO_1101, LPWKSTA_USER_INFO_1101, LPWKSTA_USER_INFO_1101 structure pointer [Network Management], PWKSTA_USER_INFO_1101, PWKSTA_USER_INFO_1101 structure pointer [Network Management], WKSTA_USER_INFO_1101, WKSTA_USER_INFO_1101 structure [Network Management], _win32_wksta_user_info_1101_str, lmwksta/LPWKSTA_USER_INFO_1101, lmwksta/PWKSTA_USER_INFO_1101, lmwksta/WKSTA_USER_INFO_1101, netmgmt.wksta_user_info_1101_str"
ms.topic: struct
f1_keywords: 
 - "lmwksta/WKSTA_USER_INFO_1101"
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
 - WKSTA_USER_INFO_1101
product: Windows
targetos: Windows
req.typenames: WKSTA_USER_INFO_1101, *PWKSTA_USER_INFO_1101, *LPWKSTA_USER_INFO_1101
req.redist: 
ms.custom: 19H1
---

# WKSTA_USER_INFO_1101 structure


## -description


The
				<b>WKSTA_USER_INFO_1101</b> structure contains information about the domains accessed by a workstation.


## -struct-fields




### -field wkui1101_oth_domains

Specifies the list of operating system domains browsed by the workstation. The domain names are separated by blanks.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/lmwksta/nf-lmwksta-netwkstausergetinfo">NetWkstaUserGetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmwksta/nf-lmwksta-netwkstausersetinfo">NetWkstaUserSetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/workstation-and-workstation-user-functions">Workstation and Workstation User Functions</a>
 

 

