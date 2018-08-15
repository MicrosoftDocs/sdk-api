---
UID: NS:lmaccess._USER_INFO_1009
title: "_USER_INFO_1009"
author: windows-sdk-content
description: The USER_INFO_1009 structure contains the path for a user's logon script file. This information level is valid only when you call the NetUserSetInfo function.
old-location: netmgmt\user_info_1009_str.htm
old-project: netmgmt
ms.assetid: baaabbf9-9571-49db-bf38-a3fc2d0a200a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPUSER_INFO_1009, *PUSER_INFO_1009, LPUSER_INFO_1009, LPUSER_INFO_1009 structure pointer [Network Management], PUSER_INFO_1009, PUSER_INFO_1009 structure pointer [Network Management], USER_INFO_1009, USER_INFO_1009 structure [Network Management], _USER_INFO_1009, _win32_user_info_1009_str, lmaccess/LPUSER_INFO_1009, lmaccess/PUSER_INFO_1009, lmaccess/USER_INFO_1009, netmgmt.user_info_1009_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lmaccess.h
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
req.typenames: USER_INFO_1009, *PUSER_INFO_1009, *LPUSER_INFO_1009
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - USER_INFO_1009
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _USER_INFO_1009 structure


## -description


The
				<b>USER_INFO_1009</b> structure contains the path for a user's logon script file. This information level is valid only when you call the 
<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> function.


## -struct-fields




### -field usri1009_script_path

Pointer to a Unicode string specifying the path for the user's logon script file. The user is specified in the <i>username</i> parameter to the 
<b>NetUserSetInfo</b> function. The script file can be a .CMD file, an .EXE file, or a .BAT file. The string can also be null.


## -see-also




<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/cf0e5102-3924-46c0-8124-0aa04e95f48d">User Functions</a>
 

 

