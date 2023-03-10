---
UID: NS:lmaccess._USER_MODALS_INFO_1005
title: USER_MODALS_INFO_1005 (lmaccess.h)
description: The USER_MODALS_INFO_1005 structure contains password history information for users and global groups in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.
helpviewer_keywords: ["*LPUSER_MODALS_INFO_1005","*PUSER_MODALS_INFO_1005","LPUSER_MODALS_INFO_1005","LPUSER_MODALS_INFO_1005 structure pointer [Network Management]","PUSER_MODALS_INFO_1005","PUSER_MODALS_INFO_1005 structure pointer [Network Management]","USER_MODALS_INFO_1005","USER_MODALS_INFO_1005 structure [Network Management]","_win32_user_modals_info_1005_str","lmaccess/LPUSER_MODALS_INFO_1005","lmaccess/PUSER_MODALS_INFO_1005","lmaccess/USER_MODALS_INFO_1005","netmgmt.user_modals_info_1005_str"]
old-location: netmgmt\user_modals_info_1005_str.htm
tech.root: NetMgmt
ms.assetid: 0156443a-e126-4aa5-a248-9ff55ff53771
ms.date: 12/05/2018
ms.keywords: '*LPUSER_MODALS_INFO_1005, *PUSER_MODALS_INFO_1005, LPUSER_MODALS_INFO_1005, LPUSER_MODALS_INFO_1005 structure pointer [Network Management], PUSER_MODALS_INFO_1005, PUSER_MODALS_INFO_1005 structure pointer [Network Management], USER_MODALS_INFO_1005, USER_MODALS_INFO_1005 structure [Network Management], _win32_user_modals_info_1005_str, lmaccess/LPUSER_MODALS_INFO_1005, lmaccess/PUSER_MODALS_INFO_1005, lmaccess/USER_MODALS_INFO_1005, netmgmt.user_modals_info_1005_str'
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
req.typenames: USER_MODALS_INFO_1005, *PUSER_MODALS_INFO_1005, *LPUSER_MODALS_INFO_1005
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_MODALS_INFO_1005
 - lmaccess/_USER_MODALS_INFO_1005
 - PUSER_MODALS_INFO_1005
 - lmaccess/PUSER_MODALS_INFO_1005
 - USER_MODALS_INFO_1005
 - lmaccess/USER_MODALS_INFO_1005
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
 - USER_MODALS_INFO_1005
---

# USER_MODALS_INFO_1005 structure


## -description

The 
				<b>USER_MODALS_INFO_1005</b> structure contains password history information for users and global groups in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.

## -struct-fields

### -field usrmod1005_password_hist_len

Specifies the length of password history that the system maintains. A new password cannot match any of the previous usrmod<i>X</i>_password_hist_len passwords. Valid values for this element are zero through DEF_MAX_PWHIST.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusermodalsset">NetUserModalsSet</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-modal-functions">User Modal Functions</a>