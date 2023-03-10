---
UID: NS:lmaccess._USER_MODALS_INFO_1007
title: USER_MODALS_INFO_1007 (lmaccess.h)
description: The USER_MODALS_INFO_1007 structure contains domain controller information.
helpviewer_keywords: ["*LPUSER_MODALS_INFO_1007","*PUSER_MODALS_INFO_1007","LPUSER_MODALS_INFO_1007","LPUSER_MODALS_INFO_1007 structure pointer [Network Management]","PUSER_MODALS_INFO_1007","PUSER_MODALS_INFO_1007 structure pointer [Network Management]","USER_MODALS_INFO_1007","USER_MODALS_INFO_1007 structure [Network Management]","_win32_user_modals_info_1007_str","lmaccess/LPUSER_MODALS_INFO_1007","lmaccess/PUSER_MODALS_INFO_1007","lmaccess/USER_MODALS_INFO_1007","netmgmt.user_modals_info_1007_str"]
old-location: netmgmt\user_modals_info_1007_str.htm
tech.root: NetMgmt
ms.assetid: aa6425eb-576c-4f6f-b9c9-96d9535bc7d6
ms.date: 12/05/2018
ms.keywords: '*LPUSER_MODALS_INFO_1007, *PUSER_MODALS_INFO_1007, LPUSER_MODALS_INFO_1007, LPUSER_MODALS_INFO_1007 structure pointer [Network Management], PUSER_MODALS_INFO_1007, PUSER_MODALS_INFO_1007 structure pointer [Network Management], USER_MODALS_INFO_1007, USER_MODALS_INFO_1007 structure [Network Management], _win32_user_modals_info_1007_str, lmaccess/LPUSER_MODALS_INFO_1007, lmaccess/PUSER_MODALS_INFO_1007, lmaccess/USER_MODALS_INFO_1007, netmgmt.user_modals_info_1007_str'
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
req.typenames: USER_MODALS_INFO_1007, *PUSER_MODALS_INFO_1007, *LPUSER_MODALS_INFO_1007
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_MODALS_INFO_1007
 - lmaccess/_USER_MODALS_INFO_1007
 - PUSER_MODALS_INFO_1007
 - lmaccess/PUSER_MODALS_INFO_1007
 - USER_MODALS_INFO_1007
 - lmaccess/USER_MODALS_INFO_1007
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
 - USER_MODALS_INFO_1007
---

# USER_MODALS_INFO_1007 structure


## -description

The 
				<b>USER_MODALS_INFO_1007</b> structure contains domain controller information.

## -struct-fields

### -field usrmod1007_primary

Pointer to a Unicode string that specifies the name of the domain controller that stores the primary copy of the database for the user account manager.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusermodalsset">NetUserModalsSet</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-modal-functions">User Modal Functions</a>