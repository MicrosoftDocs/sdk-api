---
UID: NS:lmaccess._USER_MODALS_INFO_1004
title: USER_MODALS_INFO_1004 (lmaccess.h)
description: The USER_MODALS_INFO_1004 structure contains forced logoff information for users and global groups in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.
helpviewer_keywords: ["*LPUSER_MODALS_INFO_1004","*PUSER_MODALS_INFO_1004","LPUSER_MODALS_INFO_1004","LPUSER_MODALS_INFO_1004 structure pointer [Network Management]","PUSER_MODALS_INFO_1004","PUSER_MODALS_INFO_1004 structure pointer [Network Management]","USER_MODALS_INFO_1004","USER_MODALS_INFO_1004 structure [Network Management]","_win32_user_modals_info_1004_str","lmaccess/LPUSER_MODALS_INFO_1004","lmaccess/PUSER_MODALS_INFO_1004","lmaccess/USER_MODALS_INFO_1004","netmgmt.user_modals_info_1004_str"]
old-location: netmgmt\user_modals_info_1004_str.htm
tech.root: NetMgmt
ms.assetid: c11a3c94-940e-474f-9251-a32ea098788d
ms.date: 12/05/2018
ms.keywords: '*LPUSER_MODALS_INFO_1004, *PUSER_MODALS_INFO_1004, LPUSER_MODALS_INFO_1004, LPUSER_MODALS_INFO_1004 structure pointer [Network Management], PUSER_MODALS_INFO_1004, PUSER_MODALS_INFO_1004 structure pointer [Network Management], USER_MODALS_INFO_1004, USER_MODALS_INFO_1004 structure [Network Management], _win32_user_modals_info_1004_str, lmaccess/LPUSER_MODALS_INFO_1004, lmaccess/PUSER_MODALS_INFO_1004, lmaccess/USER_MODALS_INFO_1004, netmgmt.user_modals_info_1004_str'
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
req.typenames: USER_MODALS_INFO_1004, *PUSER_MODALS_INFO_1004, *LPUSER_MODALS_INFO_1004
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_MODALS_INFO_1004
 - lmaccess/_USER_MODALS_INFO_1004
 - PUSER_MODALS_INFO_1004
 - lmaccess/PUSER_MODALS_INFO_1004
 - USER_MODALS_INFO_1004
 - lmaccess/USER_MODALS_INFO_1004
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
 - USER_MODALS_INFO_1004
---

# USER_MODALS_INFO_1004 structure


## -description

The 
				<b>USER_MODALS_INFO_1004</b> structure contains forced logoff information for users and global groups in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.

## -struct-fields

### -field usrmod1004_force_logoff

Specifies, in seconds, the amount of time between the end of the valid logon time and the time when the user is forced to log off the network. A value of TIMEQ_FOREVER indicates that the user is never forced to log off. A value of zero indicates that the user will be forced to log off immediately when the valid logon time expires.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusermodalsset">NetUserModalsSet</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-modal-functions">User Modal Functions</a>