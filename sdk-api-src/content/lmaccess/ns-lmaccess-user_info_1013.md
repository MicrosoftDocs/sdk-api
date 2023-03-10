---
UID: NS:lmaccess._USER_INFO_1013
title: USER_INFO_1013 (lmaccess.h)
description: The USER_INFO_1013 structure contains reserved information for network accounts. This information level is valid only when you call the NetUserSetInfo function.
helpviewer_keywords: ["*LPUSER_INFO_1013","*PUSER_INFO_1013","LPUSER_INFO_1013","LPUSER_INFO_1013 structure pointer [Network Management]","PUSER_INFO_1013","PUSER_INFO_1013 structure pointer [Network Management]","USER_INFO_1013","USER_INFO_1013 structure [Network Management]","_win32_user_info_1013_str","lmaccess/LPUSER_INFO_1013","lmaccess/PUSER_INFO_1013","lmaccess/USER_INFO_1013","netmgmt.user_info_1013_str"]
old-location: netmgmt\user_info_1013_str.htm
tech.root: NetMgmt
ms.assetid: 7166201d-57e3-4288-ad15-392cc3733dc6
ms.date: 12/05/2018
ms.keywords: '*LPUSER_INFO_1013, *PUSER_INFO_1013, LPUSER_INFO_1013, LPUSER_INFO_1013 structure pointer [Network Management], PUSER_INFO_1013, PUSER_INFO_1013 structure pointer [Network Management], USER_INFO_1013, USER_INFO_1013 structure [Network Management], _win32_user_info_1013_str, lmaccess/LPUSER_INFO_1013, lmaccess/PUSER_INFO_1013, lmaccess/USER_INFO_1013, netmgmt.user_info_1013_str'
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
req.typenames: USER_INFO_1013, *PUSER_INFO_1013, *LPUSER_INFO_1013
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_INFO_1013
 - lmaccess/_USER_INFO_1013
 - PUSER_INFO_1013
 - lmaccess/PUSER_INFO_1013
 - USER_INFO_1013
 - lmaccess/USER_INFO_1013
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
 - USER_INFO_1013
---

# USER_INFO_1013 structure


## -description

The
				<b>USER_INFO_1013</b> structure contains reserved information for network accounts. This information level is valid only when you call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function.

## -struct-fields

### -field usri1013_parms

Pointer to a Unicode string that is reserved for use by applications. The string can be a null string, or it can have any number of characters before the terminating null character. Microsoft products use this member to store user configuration information. Do not modify this information. 




The system components that use this member are services for Macintosh, file and print services for NetWare, and the Remote Access Server (RAS).

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>