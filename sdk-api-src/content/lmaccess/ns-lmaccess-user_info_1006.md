---
UID: NS:lmaccess._USER_INFO_1006
title: USER_INFO_1006 (lmaccess.h)
description: The USER_INFO_1006 structure contains the user's home directory path. This information level is valid only when you call the NetUserSetInfo function.
helpviewer_keywords: ["*LPUSER_INFO_1006","*PUSER_INFO_1006","LPUSER_INFO_1006","LPUSER_INFO_1006 structure pointer [Network Management]","PUSER_INFO_1006","PUSER_INFO_1006 structure pointer [Network Management]","USER_INFO_1006","USER_INFO_1006 structure [Network Management]","_win32_user_info_1006_str","lmaccess/LPUSER_INFO_1006","lmaccess/PUSER_INFO_1006","lmaccess/USER_INFO_1006","netmgmt.user_info_1006_str"]
old-location: netmgmt\user_info_1006_str.htm
tech.root: NetMgmt
ms.assetid: 9eb4973b-cda5-4862-b558-3af90b7de19f
ms.date: 12/05/2018
ms.keywords: '*LPUSER_INFO_1006, *PUSER_INFO_1006, LPUSER_INFO_1006, LPUSER_INFO_1006 structure pointer [Network Management], PUSER_INFO_1006, PUSER_INFO_1006 structure pointer [Network Management], USER_INFO_1006, USER_INFO_1006 structure [Network Management], _win32_user_info_1006_str, lmaccess/LPUSER_INFO_1006, lmaccess/PUSER_INFO_1006, lmaccess/USER_INFO_1006, netmgmt.user_info_1006_str'
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
req.typenames: USER_INFO_1006, *PUSER_INFO_1006, *LPUSER_INFO_1006
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_INFO_1006
 - lmaccess/_USER_INFO_1006
 - PUSER_INFO_1006
 - lmaccess/PUSER_INFO_1006
 - USER_INFO_1006
 - lmaccess/USER_INFO_1006
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
 - USER_INFO_1006
---

# USER_INFO_1006 structure


## -description

The
				<b>USER_INFO_1006</b> structure contains the user's home directory path. This information level is valid only when you call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function.

## -struct-fields

### -field usri1006_home_dir

Pointer to a Unicode string specifying the path of the home directory for the user account specified in the <i>username</i> parameter to the 
<b>NetUserSetInfo</b> function. The string can be null.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>