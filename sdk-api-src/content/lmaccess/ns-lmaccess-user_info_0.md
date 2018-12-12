---
UID: NS:lmaccess._USER_INFO_0
title: USER_INFO_0
author: windows-sdk-content
description: The USER_INFO_0 structure contains a user account name.
old-location: netmgmt\user_info_0_str.htm
tech.root: netmgmt
ms.assetid: 5d24a2dd-d1ee-4c97-8fbc-0b336313b60c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPUSER_INFO_0, *PUSER_INFO_0, LPUSER_INFO_0, LPUSER_INFO_0 structure pointer [Network Management], PUSER_INFO_0, PUSER_INFO_0 structure pointer [Network Management], USER_INFO_0, USER_INFO_0 structure [Network Management], _win32_user_info_0_str, lmaccess/LPUSER_INFO_0, lmaccess/PUSER_INFO_0, lmaccess/USER_INFO_0, netmgmt.user_info_0_str"
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
 - USER_INFO_0
product: Windows
targetos: Windows
req.typenames: USER_INFO_0, *PUSER_INFO_0, *LPUSER_INFO_0
req.redist: 
---

# USER_INFO_0 structure


## -description


The
				<b>USER_INFO_0</b> structure contains a user account name.


## -struct-fields




### -field usri0_name

Pointer to a Unicode string that specifies the name of the user account. For the 
<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> function, this member specifies the name of the user.


## -remarks



User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.




## -see-also




<a href="https://msdn.microsoft.com/200b0640-71e9-4f60-bf4c-c8df10bfe095">NetUseDel</a>



<a href="https://msdn.microsoft.com/b26ef3c0-934a-4840-8c06-4eaff5c9ff86">NetUserEnum</a>



<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/cf0e5102-3924-46c0-8124-0aa04e95f48d">User Functions</a>
 

 

