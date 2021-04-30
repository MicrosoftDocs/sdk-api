---
UID: NS:lmaccess._USER_MODALS_INFO_3
title: USER_MODALS_INFO_3 (lmaccess.h)
description: The USER_MODALS_INFO_3 structure contains lockout information for users and global groups in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.
helpviewer_keywords: ["*LPUSER_MODALS_INFO_3","*PUSER_MODALS_INFO_3","LPUSER_MODALS_INFO_3","LPUSER_MODALS_INFO_3 structure pointer [Network Management]","PUSER_MODALS_INFO_3","PUSER_MODALS_INFO_3 structure pointer [Network Management]","USER_MODALS_INFO_3","USER_MODALS_INFO_3 structure [Network Management]","_win32_user_modals_info_3_str","lmaccess/LPUSER_MODALS_INFO_3","lmaccess/PUSER_MODALS_INFO_3","lmaccess/USER_MODALS_INFO_3","netmgmt.user_modals_info_3_str"]
old-location: netmgmt\user_modals_info_3_str.htm
tech.root: NetMgmt
ms.assetid: 39f85712-1afd-4e34-8e7b-0938a7a48234
ms.date: 12/05/2018
ms.keywords: '*LPUSER_MODALS_INFO_3, *PUSER_MODALS_INFO_3, LPUSER_MODALS_INFO_3, LPUSER_MODALS_INFO_3 structure pointer [Network Management], PUSER_MODALS_INFO_3, PUSER_MODALS_INFO_3 structure pointer [Network Management], USER_MODALS_INFO_3, USER_MODALS_INFO_3 structure [Network Management], _win32_user_modals_info_3_str, lmaccess/LPUSER_MODALS_INFO_3, lmaccess/PUSER_MODALS_INFO_3, lmaccess/USER_MODALS_INFO_3, netmgmt.user_modals_info_3_str'
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
req.typenames: USER_MODALS_INFO_3, *PUSER_MODALS_INFO_3, *LPUSER_MODALS_INFO_3
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_MODALS_INFO_3
 - lmaccess/_USER_MODALS_INFO_3
 - PUSER_MODALS_INFO_3
 - lmaccess/PUSER_MODALS_INFO_3
 - USER_MODALS_INFO_3
 - lmaccess/USER_MODALS_INFO_3
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
 - USER_MODALS_INFO_3
---

# USER_MODALS_INFO_3 structure


## -description

The
				<b>USER_MODALS_INFO_3</b> structure contains lockout information for users and global groups in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.

## -struct-fields

### -field usrmod3_lockout_duration

Specifies, in seconds, how long a locked account remains locked before it is automatically unlocked.

### -field usrmod3_lockout_observation_window

Specifies the maximum time, in seconds, that can elapse between any two failed logon attempts before lockout occurs.

### -field usrmod3_lockout_threshold

Specifies the number of invalid password authentications that can occur before an account is marked "locked out."

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusermodalsget">NetUserModalsGet</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusermodalsset">NetUserModalsSet</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-modal-functions">User Modal Functions</a>