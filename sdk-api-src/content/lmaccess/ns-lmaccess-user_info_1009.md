---
UID: NS:lmaccess._USER_INFO_1009
title: USER_INFO_1009 (lmaccess.h)
description: The USER_INFO_1009 structure contains the path for a user's logon script file. This information level is valid only when you call the NetUserSetInfo function.
helpviewer_keywords: ["*LPUSER_INFO_1009","*PUSER_INFO_1009","LPUSER_INFO_1009","LPUSER_INFO_1009 structure pointer [Network Management]","PUSER_INFO_1009","PUSER_INFO_1009 structure pointer [Network Management]","USER_INFO_1009","USER_INFO_1009 structure [Network Management]","_win32_user_info_1009_str","lmaccess/LPUSER_INFO_1009","lmaccess/PUSER_INFO_1009","lmaccess/USER_INFO_1009","netmgmt.user_info_1009_str"]
old-location: netmgmt\user_info_1009_str.htm
tech.root: NetMgmt
ms.assetid: baaabbf9-9571-49db-bf38-a3fc2d0a200a
ms.date: 12/05/2018
ms.keywords: '*LPUSER_INFO_1009, *PUSER_INFO_1009, LPUSER_INFO_1009, LPUSER_INFO_1009 structure pointer [Network Management], PUSER_INFO_1009, PUSER_INFO_1009 structure pointer [Network Management], USER_INFO_1009, USER_INFO_1009 structure [Network Management], _win32_user_info_1009_str, lmaccess/LPUSER_INFO_1009, lmaccess/PUSER_INFO_1009, lmaccess/USER_INFO_1009, netmgmt.user_info_1009_str'
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
req.typenames: USER_INFO_1009, *PUSER_INFO_1009, *LPUSER_INFO_1009
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_INFO_1009
 - lmaccess/_USER_INFO_1009
 - PUSER_INFO_1009
 - lmaccess/PUSER_INFO_1009
 - USER_INFO_1009
 - lmaccess/USER_INFO_1009
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
 - USER_INFO_1009
---

# USER_INFO_1009 structure


## -description

The
				<b>USER_INFO_1009</b> structure contains the path for a user's logon script file. This information level is valid only when you call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function.

## -struct-fields

### -field usri1009_script_path

Pointer to a Unicode string specifying the path for the user's logon script file. The user is specified in the <i>username</i> parameter to the 
<b>NetUserSetInfo</b> function. The script file can be a .CMD file, an .EXE file, or a .BAT file. The string can also be null.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>