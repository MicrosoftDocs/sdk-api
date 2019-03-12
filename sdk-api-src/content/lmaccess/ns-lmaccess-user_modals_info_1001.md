---
UID: NS:lmaccess._USER_MODALS_INFO_1001
title: USER_MODALS_INFO_1001
author: windows-sdk-content
description: The USER_MODALS_INFO_1001 structure contains the minimum length for passwords in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.
old-location: netmgmt\user_modals_info_1001_str.htm
tech.root: NetMgmt
ms.assetid: ef6e63da-f092-4435-93f0-e50d2fdd5664
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPUSER_MODALS_INFO_1001, *PUSER_MODALS_INFO_1001, LPUSER_MODALS_INFO_1001, LPUSER_MODALS_INFO_1001 structure pointer [Network Management], PUSER_MODALS_INFO_1001, PUSER_MODALS_INFO_1001 structure pointer [Network Management], USER_MODALS_INFO_1001, USER_MODALS_INFO_1001 structure [Network Management], _win32_user_modals_info_1001_str, lmaccess/LPUSER_MODALS_INFO_1001, lmaccess/PUSER_MODALS_INFO_1001, lmaccess/USER_MODALS_INFO_1001, netmgmt.user_modals_info_1001_str"
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
 - USER_MODALS_INFO_1001
product: Windows
targetos: Windows
req.typenames: USER_MODALS_INFO_1001, *PUSER_MODALS_INFO_1001, *LPUSER_MODALS_INFO_1001
req.redist: 
---

# USER_MODALS_INFO_1001 structure


## -description


The 
				<b>USER_MODALS_INFO_1001</b> structure contains the minimum length for passwords in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.


## -struct-fields




### -field usrmod1001_min_passwd_len

Specifies the minimum allowable password length. Valid values for this element are zero through PWLEN.


## -see-also




<a href="https://msdn.microsoft.com/9884e076-ee6a-4aca-abe6-a79754667759">NetUserModalsSet</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/e655b9f6-2808-4bd4-998c-c8a2e980920b">User Modal Functions</a>
 

 

