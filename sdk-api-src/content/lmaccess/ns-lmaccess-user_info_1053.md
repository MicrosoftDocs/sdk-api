---
UID: NS:lmaccess._USER_INFO_1053
title: USER_INFO_1053 (lmaccess.h)
description: The USER_INFO_1053 structure contains user information for network accounts. This information level is valid only when you call the NetUserSetInfo function.
helpviewer_keywords: ["*LPUSER_INFO_1053","*PUSER_INFO_1053","LPUSER_INFO_1053","LPUSER_INFO_1053 structure pointer [Network Management]","PUSER_INFO_1053","PUSER_INFO_1053 structure pointer [Network Management]","USER_INFO_1053","USER_INFO_1053 structure [Network Management]","_win32_user_info_1053_str","lmaccess/LPUSER_INFO_1053","lmaccess/PUSER_INFO_1053","lmaccess/USER_INFO_1053","netmgmt.user_info_1053_str"]
old-location: netmgmt\user_info_1053_str.htm
tech.root: NetMgmt
ms.assetid: 687b2c35-344d-49db-a1e2-fb5c2b5db2d6
ms.date: 12/05/2018
ms.keywords: '*LPUSER_INFO_1053, *PUSER_INFO_1053, LPUSER_INFO_1053, LPUSER_INFO_1053 structure pointer [Network Management], PUSER_INFO_1053, PUSER_INFO_1053 structure pointer [Network Management], USER_INFO_1053, USER_INFO_1053 structure [Network Management], _win32_user_info_1053_str, lmaccess/LPUSER_INFO_1053, lmaccess/PUSER_INFO_1053, lmaccess/USER_INFO_1053, netmgmt.user_info_1053_str'
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
req.typenames: USER_INFO_1053, *PUSER_INFO_1053, *LPUSER_INFO_1053
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_INFO_1053
 - lmaccess/_USER_INFO_1053
 - PUSER_INFO_1053
 - lmaccess/PUSER_INFO_1053
 - USER_INFO_1053
 - lmaccess/USER_INFO_1053
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
 - USER_INFO_1053
---

# USER_INFO_1053 structure


## -description

The
				<b>USER_INFO_1053</b> structure contains user information for network accounts. This information level is valid only when you call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function.

## -struct-fields

### -field usri1053_home_dir_drive

Specifies the drive letter to assign to the user's home directory for logon purposes. The user is specified in the <i>username</i> parameter to the 
<b>NetUserSetInfo</b> function.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>