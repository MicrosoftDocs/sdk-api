---
UID: NS:lmaccess._USER_MODALS_INFO_1003
title: USER_MODALS_INFO_1003 (lmaccess.h)
description: The USER_MODALS_INFO_1003 structure contains the minimum duration for passwords in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.
helpviewer_keywords: ["*LPUSER_MODALS_INFO_1003","*PUSER_MODALS_INFO_1003","LPUSER_MODALS_INFO_1003","LPUSER_MODALS_INFO_1003 structure pointer [Network Management]","PUSER_MODALS_INFO_1003","PUSER_MODALS_INFO_1003 structure pointer [Network Management]","USER_MODALS_INFO_1003","USER_MODALS_INFO_1003 structure [Network Management]","_win32_user_modals_info_1003_str","lmaccess/LPUSER_MODALS_INFO_1003","lmaccess/PUSER_MODALS_INFO_1003","lmaccess/USER_MODALS_INFO_1003","netmgmt.user_modals_info_1003_str"]
old-location: netmgmt\user_modals_info_1003_str.htm
tech.root: NetMgmt
ms.assetid: 5efbba0f-b871-4ffa-8e83-abeab6b70a52
ms.date: 12/05/2018
ms.keywords: '*LPUSER_MODALS_INFO_1003, *PUSER_MODALS_INFO_1003, LPUSER_MODALS_INFO_1003, LPUSER_MODALS_INFO_1003 structure pointer [Network Management], PUSER_MODALS_INFO_1003, PUSER_MODALS_INFO_1003 structure pointer [Network Management], USER_MODALS_INFO_1003, USER_MODALS_INFO_1003 structure [Network Management], _win32_user_modals_info_1003_str, lmaccess/LPUSER_MODALS_INFO_1003, lmaccess/PUSER_MODALS_INFO_1003, lmaccess/USER_MODALS_INFO_1003, netmgmt.user_modals_info_1003_str'
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
targetos: Windows
req.typenames: USER_MODALS_INFO_1003, *PUSER_MODALS_INFO_1003, *LPUSER_MODALS_INFO_1003
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_MODALS_INFO_1003
 - lmaccess/_USER_MODALS_INFO_1003
 - PUSER_MODALS_INFO_1003
 - lmaccess/PUSER_MODALS_INFO_1003
 - USER_MODALS_INFO_1003
 - lmaccess/USER_MODALS_INFO_1003
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - USER_MODALS_INFO_1003
---

# USER_MODALS_INFO_1003 structure


## -description

The 
				<b>USER_MODALS_INFO_1003</b> structure contains the minimum duration for passwords in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.

## -struct-fields

### -field usrmod1003_min_passwd_age

Specifies the minimum number of seconds that can elapse between the time a password changes and when it can be changed again. A value of zero indicates that no delay is required between password updates. The value specified must be less than or equal to the value for the usrmod<i>X</i>_max_passwd_age member.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusermodalsset">NetUserModalsSet</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-modal-functions">User Modal Functions</a>