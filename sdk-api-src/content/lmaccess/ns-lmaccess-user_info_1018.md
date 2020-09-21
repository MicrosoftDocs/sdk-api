---
UID: NS:lmaccess._USER_INFO_1018
title: USER_INFO_1018 (lmaccess.h)
description: The USER_INFO_1018 structure contains the maximum amount of disk space available to a network user account. This information level is valid only when you call the NetUserSetInfo function.
helpviewer_keywords: ["*LPUSER_INFO_1018","*PUSER_INFO_1018","LPUSER_INFO_1018","LPUSER_INFO_1018 structure pointer [Network Management]","PUSER_INFO_1018","PUSER_INFO_1018 structure pointer [Network Management]","USER_INFO_1018","USER_INFO_1018 structure [Network Management]","_win32_user_info_1018_str","lmaccess/LPUSER_INFO_1018","lmaccess/PUSER_INFO_1018","lmaccess/USER_INFO_1018","netmgmt.user_info_1018_str"]
old-location: netmgmt\user_info_1018_str.htm
tech.root: NetMgmt
ms.assetid: 15bdff5c-a360-4519-8e0b-c73ddd01298c
ms.date: 12/05/2018
ms.keywords: '*LPUSER_INFO_1018, *PUSER_INFO_1018, LPUSER_INFO_1018, LPUSER_INFO_1018 structure pointer [Network Management], PUSER_INFO_1018, PUSER_INFO_1018 structure pointer [Network Management], USER_INFO_1018, USER_INFO_1018 structure [Network Management], _win32_user_info_1018_str, lmaccess/LPUSER_INFO_1018, lmaccess/PUSER_INFO_1018, lmaccess/USER_INFO_1018, netmgmt.user_info_1018_str'
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
req.typenames: USER_INFO_1018, *PUSER_INFO_1018, *LPUSER_INFO_1018
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_INFO_1018
 - lmaccess/_USER_INFO_1018
 - PUSER_INFO_1018
 - lmaccess/PUSER_INFO_1018
 - USER_INFO_1018
 - lmaccess/USER_INFO_1018
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
 - USER_INFO_1018
---

# USER_INFO_1018 structure


## -description

The
				<b>USER_INFO_1018</b> structure contains the maximum amount of disk space available to a network user account. This information level is valid only when you call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function.

## -struct-fields

### -field usri1018_max_storage

Specifies a <b>DWORD</b> value that indicates the maximum amount of disk space the user can use. The user is specified in the <i>username</i> parameter to the 
<b>NetUserSetInfo</b> function. 




You must specify USER_MAXSTORAGE_UNLIMITED to indicate that there is no restriction on disk space.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>