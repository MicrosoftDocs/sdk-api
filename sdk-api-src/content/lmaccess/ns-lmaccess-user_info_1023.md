---
UID: NS:lmaccess._USER_INFO_1023
title: USER_INFO_1023
author: windows-sdk-content
description: The USER_INFO_1023 structure contains the name of the server to which network logon requests should be sent. This information level is valid only when you call the NetUserSetInfo function.
old-location: netmgmt\user_info_1023_str.htm
tech.root: netmgmt
ms.assetid: 44985bbe-48d2-4fe9-9247-2800089269cb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPUSER_INFO_1023, *PUSER_INFO_1023, LPUSER_INFO_1023, LPUSER_INFO_1023 structure pointer [Network Management], PUSER_INFO_1023, PUSER_INFO_1023 structure pointer [Network Management], USER_INFO_1023, USER_INFO_1023 structure [Network Management], _win32_user_info_1023_str, lmaccess/LPUSER_INFO_1023, lmaccess/PUSER_INFO_1023, lmaccess/USER_INFO_1023, netmgmt.user_info_1023_str"
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
 - USER_INFO_1023
product: Windows
targetos: Windows
req.typenames: USER_INFO_1023, *PUSER_INFO_1023, *LPUSER_INFO_1023
req.redist: 
---

# USER_INFO_1023 structure


## -description


The
				<b>USER_INFO_1023</b> structure contains the name of the server to which network logon requests should be sent. This information level is valid only when you call the 
<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> function.


## -struct-fields




### -field usri1023_logon_server

Pointer to a Unicode string that contains the name of the server to which logon requests for the user account should be sent. The user account is specified in the <i>username</i> parameter to the 
<b>NetUserSetInfo</b> function. 




Server names should be preceded by two backslashes (\\). To indicate that the logon request can be handled by any logon server, specify an asterisk (\\*) for the server name. A null string indicates that requests should be sent to the domain controller.


## -see-also




<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/cf0e5102-3924-46c0-8124-0aa04e95f48d">User Functions</a>
 

 

