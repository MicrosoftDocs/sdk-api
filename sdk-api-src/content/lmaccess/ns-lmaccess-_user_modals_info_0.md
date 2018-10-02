---
UID: NS:lmaccess._USER_MODALS_INFO_0
title: "_USER_MODALS_INFO_0"
author: windows-sdk-content
description: The USER_MODALS_INFO_0 structure contains global password information for users and global groups in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.
old-location: netmgmt\user_modals_info_0_str.htm
tech.root: NetMgmt
ms.assetid: cf3dd091-106e-4a0d-b4db-62bd11fd65cf
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPUSER_MODALS_INFO_0, *PUSER_MODALS_INFO_0, LPUSER_MODALS_INFO_0, LPUSER_MODALS_INFO_0 structure pointer [Network Management], PUSER_MODALS_INFO_0, PUSER_MODALS_INFO_0 structure pointer [Network Management], USER_MODALS_INFO_0, USER_MODALS_INFO_0 structure [Network Management], _USER_MODALS_INFO_0, _win32_user_modals_info_0_str, lmaccess/LPUSER_MODALS_INFO_0, lmaccess/PUSER_MODALS_INFO_0, lmaccess/USER_MODALS_INFO_0, netmgmt.user_modals_info_0_str"
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
 - USER_MODALS_INFO_0
product: Windows
targetos: Windows
req.typenames: USER_MODALS_INFO_0, *PUSER_MODALS_INFO_0, *LPUSER_MODALS_INFO_0
req.redist: 
---

# _USER_MODALS_INFO_0 structure


## -description


The
				<b>USER_MODALS_INFO_0</b> structure contains global password information for users and global groups in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.


## -struct-fields




### -field usrmod0_min_passwd_len

Specifies the minimum allowable password length. Valid values for this element are zero through LM20_PWLEN.


### -field usrmod0_max_passwd_age

Specifies, in seconds, the maximum allowable password age. A value of TIMEQ_FOREVER indicates that the password never expires. The minimum valid value for this element is ONE_DAY. The value specified must be greater than or equal to the value for the <b>usrmod0_min_passwd_age</b> member.


### -field usrmod0_min_passwd_age

Specifies the minimum number of seconds that can elapse between the time a password changes and when it can be changed again. A value of zero indicates that no delay is required between password updates. The value specified must be less than or equal to the value for the <b>usrmod0_max_passwd_age</b> member.


### -field usrmod0_force_logoff

Specifies, in seconds, the amount of time between the end of the valid logon time and the time when the user is forced to log off the network. A value of TIMEQ_FOREVER indicates that the user is never forced to log off. A value of zero indicates that the user will be forced to log off immediately when the valid logon time expires.


### -field usrmod0_password_hist_len

Specifies the length of password history maintained. A new password cannot match any of the previous <b>usrmod0_password_hist_len</b> passwords. Valid values for this element are zero through DEF_MAX_PWHIST.


## -see-also




<a href="https://msdn.microsoft.com/5bb18144-82a6-4e9b-8321-c06a667bdd03">NetUserModalsGet</a>



<a href="https://msdn.microsoft.com/9884e076-ee6a-4aca-abe6-a79754667759">NetUserModalsSet</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/e655b9f6-2808-4bd4-998c-c8a2e980920b">User Modal Functions</a>
 

 

