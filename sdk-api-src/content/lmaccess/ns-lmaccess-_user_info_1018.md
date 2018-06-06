---
UID: NS:lmaccess._USER_INFO_1018
title: "_USER_INFO_1018"
author: windows-sdk-content
description: The USER_INFO_1018 structure contains the maximum amount of disk space available to a network user account. This information level is valid only when you call the NetUserSetInfo function.
old-location: netmgmt\user_info_1018_str.htm
old-project: NetMgmt
ms.assetid: 15bdff5c-a360-4519-8e0b-c73ddd01298c
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*LPUSER_INFO_1018, *PUSER_INFO_1018, LPUSER_INFO_1018, LPUSER_INFO_1018 structure pointer [Network Management], PUSER_INFO_1018, PUSER_INFO_1018 structure pointer [Network Management], USER_INFO_1018, USER_INFO_1018 structure [Network Management], _USER_INFO_1018, _win32_user_info_1018_str, lmaccess/LPUSER_INFO_1018, lmaccess/PUSER_INFO_1018, lmaccess/USER_INFO_1018, netmgmt.user_info_1018_str"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: USER_INFO_1018, *PUSER_INFO_1018, *LPUSER_INFO_1018
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - USER_INFO_1018
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _USER_INFO_1018 structure


## -description


The
				<b>USER_INFO_1018</b> structure contains the maximum amount of disk space available to a network user account. This information level is valid only when you call the 
<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> function.


## -struct-fields




### -field usri1018_max_storage

Specifies a <b>DWORD</b> value that indicates the maximum amount of disk space the user can use. The user is specified in the <i>username</i> parameter to the 
<b>NetUserSetInfo</b> function. 




You must specify USER_MAXSTORAGE_UNLIMITED to indicate that there is no restriction on disk space.


## -see-also




<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/cf0e5102-3924-46c0-8124-0aa04e95f48d">User Functions</a>
 

 

