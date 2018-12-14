---
UID: NS:lmaccess._LOCALGROUP_USERS_INFO_0
title: LOCALGROUP_USERS_INFO_0
author: windows-sdk-content
description: The LOCALGROUP_USERS_INFO_0 structure contains local group member information.
old-location: netmgmt\localgroup_users_info_0_str.htm
tech.root: netmgmt
ms.assetid: e9358f19-ec8f-4454-896c-c9fadb848378
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPLOCALGROUP_USERS_INFO_0, *PLOCALGROUP_USERS_INFO_0, LOCALGROUP_USERS_INFO_0, LOCALGROUP_USERS_INFO_0 structure [Network Management], LPLOCALGROUP_USERS_INFO_0, LPLOCALGROUP_USERS_INFO_0 structure pointer [Network Management], PLOCALGROUP_USERS_INFO_0, PLOCALGROUP_USERS_INFO_0 structure pointer [Network Management], _win32_localgroup_users_info_0_str, lmaccess/LOCALGROUP_USERS_INFO_0, lmaccess/LPLOCALGROUP_USERS_INFO_0, lmaccess/PLOCALGROUP_USERS_INFO_0, netmgmt.localgroup_users_info_0_str"
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
 - LOCALGROUP_USERS_INFO_0
product: Windows
targetos: Windows
req.typenames: LOCALGROUP_USERS_INFO_0, *PLOCALGROUP_USERS_INFO_0, *LPLOCALGROUP_USERS_INFO_0
req.redist: 
---

# LOCALGROUP_USERS_INFO_0 structure


## -description


The 
				<b>LOCALGROUP_USERS_INFO_0</b> structure contains local group member information.


## -struct-fields




### -field lgrui0_name

Pointer to a Unicode string specifying the name of a local group to which the user belongs.


## -remarks



User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.




## -see-also




<a href="https://msdn.microsoft.com/ed4c59d6-6532-4190-9807-95678053fc72">Local Group Functions</a>



<a href="https://msdn.microsoft.com/cc5c1c15-cad7-4103-a2c9-1a8adf742703">NetUserGetLocalGroups</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

