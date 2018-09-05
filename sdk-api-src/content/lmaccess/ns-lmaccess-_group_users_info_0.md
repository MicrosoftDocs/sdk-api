---
UID: NS:lmaccess._GROUP_USERS_INFO_0
title: "_GROUP_USERS_INFO_0"
author: windows-sdk-content
description: The GROUP_USERS_INFO_0 structure contains global group member information.
old-location: netmgmt\group_users_info_0_str.htm
old-project: netmgmt
ms.assetid: cc0e5d27-91f1-4640-bb80-e73899fabba9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPGROUP_USERS_INFO_0, *PGROUP_USERS_INFO_0, GROUP_USERS_INFO_0, GROUP_USERS_INFO_0 structure [Network Management], LPGROUP_USERS_INFO_0, LPGROUP_USERS_INFO_0 structure pointer [Network Management], PGROUP_USERS_INFO_0, PGROUP_USERS_INFO_0 structure pointer [Network Management], _GROUP_USERS_INFO_0, _win32_group_users_info_0_str, lmaccess/GROUP_USERS_INFO_0, lmaccess/LPGROUP_USERS_INFO_0, lmaccess/PGROUP_USERS_INFO_0, netmgmt.group_users_info_0_str"
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
req.typenames: GROUP_USERS_INFO_0, *PGROUP_USERS_INFO_0, *LPGROUP_USERS_INFO_0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - GROUP_USERS_INFO_0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _GROUP_USERS_INFO_0 structure


## -description


The
				<b>GROUP_USERS_INFO_0</b> structure contains global group member information.


## -struct-fields




### -field grui0_name

A pointer to a null-terminated Unicode character string that specifies a name. For more information, see the Remarks section.


## -remarks



If you are calling the 
<a href="https://msdn.microsoft.com/a9bcb806-f44c-4db2-9644-06687b31405d">NetGroupGetUsers</a> function or the 
<a href="https://msdn.microsoft.com/4221f5c8-a71c-4368-9be4-9562063b6cfd">NetGroupSetUsers</a> function, the <b>grui0_name</b> member contains the name of a user that is a member of the specified group.

If you are calling the 
<a href="https://msdn.microsoft.com/ecf1a94c-5dda-4f49-81bd-93e551e089f1">NetUserGetGroups</a> function or the 
<a href="https://msdn.microsoft.com/7042c43a-09d1-4179-8074-eb055dc279a6">NetUserSetGroups</a> function, the <b>grui0_name</b> member contains the name of a global group to which the specified user belongs. 

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.




## -see-also




<a href="https://msdn.microsoft.com/d92e7c18-f2c7-4ea5-8bb6-fec023272dbb">GROUP_USERS_INFO_1</a>



<a href="https://msdn.microsoft.com/2199258d-bde9-4fdb-b9c1-147616420fbe">Group Functions</a>



<a href="https://msdn.microsoft.com/a9bcb806-f44c-4db2-9644-06687b31405d">NetGroupGetUsers</a>



<a href="https://msdn.microsoft.com/4221f5c8-a71c-4368-9be4-9562063b6cfd">NetGroupSetUsers</a>



<a href="https://msdn.microsoft.com/ecf1a94c-5dda-4f49-81bd-93e551e089f1">NetUserGetGroups</a>



<a href="https://msdn.microsoft.com/5bd13bed-938a-4273-840e-99fca99f7139">NetUserGetInfo</a>



<a href="https://msdn.microsoft.com/7042c43a-09d1-4179-8074-eb055dc279a6">NetUserSetGroups</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

