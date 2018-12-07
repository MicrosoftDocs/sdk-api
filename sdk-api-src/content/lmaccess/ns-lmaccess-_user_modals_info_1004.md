---
UID: NS:lmaccess._USER_MODALS_INFO_1004
title: "_USER_MODALS_INFO_1004"
author: windows-sdk-content
description: The USER_MODALS_INFO_1004 structure contains forced logoff information for users and global groups in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.
old-location: netmgmt\user_modals_info_1004_str.htm
tech.root: netmgmt
ms.assetid: c11a3c94-940e-474f-9251-a32ea098788d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPUSER_MODALS_INFO_1004, *PUSER_MODALS_INFO_1004, LPUSER_MODALS_INFO_1004, LPUSER_MODALS_INFO_1004 structure pointer [Network Management], PUSER_MODALS_INFO_1004, PUSER_MODALS_INFO_1004 structure pointer [Network Management], USER_MODALS_INFO_1004, USER_MODALS_INFO_1004 structure [Network Management], _USER_MODALS_INFO_1004, _win32_user_modals_info_1004_str, lmaccess/LPUSER_MODALS_INFO_1004, lmaccess/PUSER_MODALS_INFO_1004, lmaccess/USER_MODALS_INFO_1004, netmgmt.user_modals_info_1004_str"
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
 - USER_MODALS_INFO_1004
product: Windows
targetos: Windows
req.typenames: USER_MODALS_INFO_1004, *PUSER_MODALS_INFO_1004, *LPUSER_MODALS_INFO_1004
req.redist: 
---

# _USER_MODALS_INFO_1004 structure


## -description


The 
				<b>USER_MODALS_INFO_1004</b> structure contains forced logoff information for users and global groups in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.


## -struct-fields




### -field usrmod1004_force_logoff

Specifies, in seconds, the amount of time between the end of the valid logon time and the time when the user is forced to log off the network. A value of TIMEQ_FOREVER indicates that the user is never forced to log off. A value of zero indicates that the user will be forced to log off immediately when the valid logon time expires.


## -see-also




<a href="https://msdn.microsoft.com/9884e076-ee6a-4aca-abe6-a79754667759">NetUserModalsSet</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/e655b9f6-2808-4bd4-998c-c8a2e980920b">User Modal Functions</a>
 

 

