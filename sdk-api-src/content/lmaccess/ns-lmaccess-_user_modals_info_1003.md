---
UID: NS:lmaccess._USER_MODALS_INFO_1003
title: "_USER_MODALS_INFO_1003"
author: windows-sdk-content
description: The USER_MODALS_INFO_1003 structure contains the minimum duration for passwords in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.
old-location: netmgmt\user_modals_info_1003_str.htm
old-project: netmgmt
ms.assetid: 5efbba0f-b871-4ffa-8e83-abeab6b70a52
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPUSER_MODALS_INFO_1003, *PUSER_MODALS_INFO_1003, LPUSER_MODALS_INFO_1003, LPUSER_MODALS_INFO_1003 structure pointer [Network Management], PUSER_MODALS_INFO_1003, PUSER_MODALS_INFO_1003 structure pointer [Network Management], USER_MODALS_INFO_1003, USER_MODALS_INFO_1003 structure [Network Management], _USER_MODALS_INFO_1003, _win32_user_modals_info_1003_str, lmaccess/LPUSER_MODALS_INFO_1003, lmaccess/PUSER_MODALS_INFO_1003, lmaccess/USER_MODALS_INFO_1003, netmgmt.user_modals_info_1003_str"
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
req.typenames: USER_MODALS_INFO_1003, *PUSER_MODALS_INFO_1003, *LPUSER_MODALS_INFO_1003
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - USER_MODALS_INFO_1003
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _USER_MODALS_INFO_1003 structure


## -description


The 
				<b>USER_MODALS_INFO_1003</b> structure contains the minimum duration for passwords in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.


## -struct-fields




### -field usrmod1003_min_passwd_age

Specifies the minimum number of seconds that can elapse between the time a password changes and when it can be changed again. A value of zero indicates that no delay is required between password updates. The value specified must be less than or equal to the value for the usrmod<i>X</i>_max_passwd_age member.


## -see-also




<a href="https://msdn.microsoft.com/9884e076-ee6a-4aca-abe6-a79754667759">NetUserModalsSet</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/e655b9f6-2808-4bd4-998c-c8a2e980920b">User Modal Functions</a>
 

 

