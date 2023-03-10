---
UID: NS:lmaccess._USER_MODALS_INFO_2
title: USER_MODALS_INFO_2 (lmaccess.h)
description: The USER_MODALS_INFO_2 structure contains the Security Account Manager (SAM) domain name and identifier.
helpviewer_keywords: ["*LPUSER_MODALS_INFO_2","*PUSER_MODALS_INFO_2","LPUSER_MODALS_INFO_2","LPUSER_MODALS_INFO_2 structure pointer [Network Management]","PUSER_MODALS_INFO_2","PUSER_MODALS_INFO_2 structure pointer [Network Management]","USER_MODALS_INFO_2","USER_MODALS_INFO_2 structure [Network Management]","_win32_user_modals_info_2_str","lmaccess/LPUSER_MODALS_INFO_2","lmaccess/PUSER_MODALS_INFO_2","lmaccess/USER_MODALS_INFO_2","netmgmt.user_modals_info_2_str"]
old-location: netmgmt\user_modals_info_2_str.htm
tech.root: NetMgmt
ms.assetid: 9a4b3fc1-03b5-4ba7-948f-e455c34fa234
ms.date: 12/05/2018
ms.keywords: '*LPUSER_MODALS_INFO_2, *PUSER_MODALS_INFO_2, LPUSER_MODALS_INFO_2, LPUSER_MODALS_INFO_2 structure pointer [Network Management], PUSER_MODALS_INFO_2, PUSER_MODALS_INFO_2 structure pointer [Network Management], USER_MODALS_INFO_2, USER_MODALS_INFO_2 structure [Network Management], _win32_user_modals_info_2_str, lmaccess/LPUSER_MODALS_INFO_2, lmaccess/PUSER_MODALS_INFO_2, lmaccess/USER_MODALS_INFO_2, netmgmt.user_modals_info_2_str'
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
req.typenames: USER_MODALS_INFO_2, *PUSER_MODALS_INFO_2, *LPUSER_MODALS_INFO_2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_MODALS_INFO_2
 - lmaccess/_USER_MODALS_INFO_2
 - PUSER_MODALS_INFO_2
 - lmaccess/PUSER_MODALS_INFO_2
 - USER_MODALS_INFO_2
 - lmaccess/USER_MODALS_INFO_2
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
 - USER_MODALS_INFO_2
---

# USER_MODALS_INFO_2 structure


## -description

The
				<b>USER_MODALS_INFO_2</b> structure contains the Security Account Manager (SAM) domain name and identifier.

## -struct-fields

### -field usrmod2_domain_name

Specifies the name of the Security Account Manager (SAM) domain. For a domain controller, this is the name of the domain that the controller is a member of. For workstations, this is the name of the computer.

### -field usrmod2_domain_id

Pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure that contains the security identifier (SID) of the domain named by the <b>usrmod2_domain_name</b> member.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusermodalsget">NetUserModalsGet</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusermodalsset">NetUserModalsSet</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-modal-functions">User Modal Functions</a>