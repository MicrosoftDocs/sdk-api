---
UID: NS:lmaccess._USER_MODALS_INFO_0
title: USER_MODALS_INFO_0 (lmaccess.h)
description: The USER_MODALS_INFO_0 structure contains global password information for users and global groups in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.
helpviewer_keywords: ["*LPUSER_MODALS_INFO_0","*PUSER_MODALS_INFO_0","LPUSER_MODALS_INFO_0","LPUSER_MODALS_INFO_0 structure pointer [Network Management]","PUSER_MODALS_INFO_0","PUSER_MODALS_INFO_0 structure pointer [Network Management]","USER_MODALS_INFO_0","USER_MODALS_INFO_0 structure [Network Management]","_win32_user_modals_info_0_str","lmaccess/LPUSER_MODALS_INFO_0","lmaccess/PUSER_MODALS_INFO_0","lmaccess/USER_MODALS_INFO_0","netmgmt.user_modals_info_0_str"]
old-location: netmgmt\user_modals_info_0_str.htm
tech.root: NetMgmt
ms.assetid: cf3dd091-106e-4a0d-b4db-62bd11fd65cf
ms.date: 12/05/2018
ms.keywords: '*LPUSER_MODALS_INFO_0, *PUSER_MODALS_INFO_0, LPUSER_MODALS_INFO_0, LPUSER_MODALS_INFO_0 structure pointer [Network Management], PUSER_MODALS_INFO_0, PUSER_MODALS_INFO_0 structure pointer [Network Management], USER_MODALS_INFO_0, USER_MODALS_INFO_0 structure [Network Management], _win32_user_modals_info_0_str, lmaccess/LPUSER_MODALS_INFO_0, lmaccess/PUSER_MODALS_INFO_0, lmaccess/USER_MODALS_INFO_0, netmgmt.user_modals_info_0_str'
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
req.typenames: USER_MODALS_INFO_0, *PUSER_MODALS_INFO_0, *LPUSER_MODALS_INFO_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_MODALS_INFO_0
 - lmaccess/_USER_MODALS_INFO_0
 - PUSER_MODALS_INFO_0
 - lmaccess/PUSER_MODALS_INFO_0
 - USER_MODALS_INFO_0
 - lmaccess/USER_MODALS_INFO_0
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
 - USER_MODALS_INFO_0
---

# USER_MODALS_INFO_0 structure


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

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusermodalsget">NetUserModalsGet</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusermodalsset">NetUserModalsSet</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-modal-functions">User Modal Functions</a>