---
UID: NS:lmaccess._USER_INFO_1006
title: "_USER_INFO_1006"
author: windows-sdk-content
description: The USER_INFO_1006 structure contains the user's home directory path. This information level is valid only when you call the NetUserSetInfo function.
old-location: netmgmt\user_info_1006_str.htm
old-project: NetMgmt
ms.assetid: 9eb4973b-cda5-4862-b558-3af90b7de19f
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*LPUSER_INFO_1006, *PUSER_INFO_1006, LPUSER_INFO_1006, LPUSER_INFO_1006 structure pointer [Network Management], PUSER_INFO_1006, PUSER_INFO_1006 structure pointer [Network Management], USER_INFO_1006, USER_INFO_1006 structure [Network Management], _USER_INFO_1006, _win32_user_info_1006_str, lmaccess/LPUSER_INFO_1006, lmaccess/PUSER_INFO_1006, lmaccess/USER_INFO_1006, netmgmt.user_info_1006_str"
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
req.typenames: USER_INFO_1006, *PUSER_INFO_1006, *LPUSER_INFO_1006
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Lmaccess.h
api_name:
-	USER_INFO_1006
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _USER_INFO_1006 structure


## -description


The
				<b>USER_INFO_1006</b> structure contains the user's home directory path. This information level is valid only when you call the 
<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> function.


## -struct-fields




### -field usri1006_home_dir

Pointer to a Unicode string specifying the path of the home directory for the user account specified in the <i>username</i> parameter to the 
<b>NetUserSetInfo</b> function. The string can be null.


## -see-also




<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/cf0e5102-3924-46c0-8124-0aa04e95f48d">User Functions</a>
 

 

