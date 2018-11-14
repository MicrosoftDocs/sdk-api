---
UID: NS:lmaccess._USER_INFO_1014
title: "_USER_INFO_1014"
author: windows-sdk-content
description: The USER_INFO_1014 structure contains the names of workstations from which the user can log on. This information level is valid only when you call the NetUserSetInfo function.
old-location: netmgmt\user_info_1014_str.htm
tech.root: NetMgmt
ms.assetid: ff7f385d-bcda-4560-b22f-d1fc94e7ae41
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPUSER_INFO_1014, *PUSER_INFO_1014, LPUSER_INFO_1014, LPUSER_INFO_1014 structure pointer [Network Management], PUSER_INFO_1014, PUSER_INFO_1014 structure pointer [Network Management], USER_INFO_1014, USER_INFO_1014 structure [Network Management], _USER_INFO_1014, _win32_user_info_1014_str, lmaccess/LPUSER_INFO_1014, lmaccess/PUSER_INFO_1014, lmaccess/USER_INFO_1014, netmgmt.user_info_1014_str"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - USER_INFO_1014
product: Windows
targetos: Windows
req.typenames: USER_INFO_1014, *PUSER_INFO_1014, *LPUSER_INFO_1014
req.redist: 
---

# _USER_INFO_1014 structure


## -description


The
				<b>USER_INFO_1014</b> structure contains the names of workstations from which the user can log on. This information level is valid only when you call the 
<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> function.


## -struct-fields




### -field usri1014_workstations

Pointer to a Unicode string that contains the names of workstations from which the user can log on. The user is specified in the <i>username</i> parameter to the 
<b>NetUserSetInfo</b> function. 




As many as eight workstations can be specified; the names must be separated by commas. A null string indicates that there is no restriction.


## -see-also




<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/cf0e5102-3924-46c0-8124-0aa04e95f48d">User Functions</a>
 

 

