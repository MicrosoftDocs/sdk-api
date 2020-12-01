---
UID: NS:lmaccess._USER_INFO_1052
title: USER_INFO_1052 (lmaccess.h)
description: The USER_INFO_1052 structure contains the path to a network user's profile. This information level is valid only when you call the NetUserSetInfo function.
helpviewer_keywords: ["*LPUSER_INFO_1052","*PUSER_INFO_1052","LPUSER_INFO_1052","LPUSER_INFO_1052 structure pointer [Network Management]","PUSER_INFO_1052","PUSER_INFO_1052 structure pointer [Network Management]","USER_INFO_1052","USER_INFO_1052 structure [Network Management]","_win32_user_info_1052_str","lmaccess/LPUSER_INFO_1052","lmaccess/PUSER_INFO_1052","lmaccess/USER_INFO_1052","netmgmt.user_info_1052_str"]
old-location: netmgmt\user_info_1052_str.htm
tech.root: NetMgmt
ms.assetid: 55ec6819-8558-413a-9a79-c2d59993163d
ms.date: 12/05/2018
ms.keywords: '*LPUSER_INFO_1052, *PUSER_INFO_1052, LPUSER_INFO_1052, LPUSER_INFO_1052 structure pointer [Network Management], PUSER_INFO_1052, PUSER_INFO_1052 structure pointer [Network Management], USER_INFO_1052, USER_INFO_1052 structure [Network Management], _win32_user_info_1052_str, lmaccess/LPUSER_INFO_1052, lmaccess/PUSER_INFO_1052, lmaccess/USER_INFO_1052, netmgmt.user_info_1052_str'
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
req.typenames: USER_INFO_1052, *PUSER_INFO_1052, *LPUSER_INFO_1052
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_INFO_1052
 - lmaccess/_USER_INFO_1052
 - PUSER_INFO_1052
 - lmaccess/PUSER_INFO_1052
 - USER_INFO_1052
 - lmaccess/USER_INFO_1052
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
 - USER_INFO_1052
---

# USER_INFO_1052 structure


## -description

The
				<b>USER_INFO_1052</b> structure contains the path to a network user's profile. This information level is valid only when you call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function.

## -struct-fields

### -field usri1052_profile

Specifies a Unicode string that contains the path to the user's profile. The user is specified in the <i>username</i> parameter to the 
<b>NetUserSetInfo</b> function. This value can be a null string, a local absolute path, or a UNC path.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>