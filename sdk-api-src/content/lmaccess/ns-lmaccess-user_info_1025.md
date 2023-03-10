---
UID: NS:lmaccess._USER_INFO_1025
title: USER_INFO_1025 (lmaccess.h)
description: The USER_INFO_1025 structure contains the code page for a network user's language of choice. This information level is valid only when you call the NetUserSetInfo function.
helpviewer_keywords: ["*LPUSER_INFO_1025","*PUSER_INFO_1025","LPUSER_INFO_1025","LPUSER_INFO_1025 structure pointer [Network Management]","PUSER_INFO_1025","PUSER_INFO_1025 structure pointer [Network Management]","USER_INFO_1025","USER_INFO_1025 structure [Network Management]","_win32_user_info_1025_str","lmaccess/LPUSER_INFO_1025","lmaccess/PUSER_INFO_1025","lmaccess/USER_INFO_1025","netmgmt.user_info_1025_str"]
old-location: netmgmt\user_info_1025_str.htm
tech.root: NetMgmt
ms.assetid: 85e3584f-8245-47e3-9e48-5c43db51be0f
ms.date: 12/05/2018
ms.keywords: '*LPUSER_INFO_1025, *PUSER_INFO_1025, LPUSER_INFO_1025, LPUSER_INFO_1025 structure pointer [Network Management], PUSER_INFO_1025, PUSER_INFO_1025 structure pointer [Network Management], USER_INFO_1025, USER_INFO_1025 structure [Network Management], _win32_user_info_1025_str, lmaccess/LPUSER_INFO_1025, lmaccess/PUSER_INFO_1025, lmaccess/USER_INFO_1025, netmgmt.user_info_1025_str'
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
req.typenames: USER_INFO_1025, *PUSER_INFO_1025, *LPUSER_INFO_1025
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_INFO_1025
 - lmaccess/_USER_INFO_1025
 - PUSER_INFO_1025
 - lmaccess/PUSER_INFO_1025
 - USER_INFO_1025
 - lmaccess/USER_INFO_1025
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
 - USER_INFO_1025
---

# USER_INFO_1025 structure


## -description

The
				<b>USER_INFO_1025</b> structure contains the code page for a network user's language of choice. This information level is valid only when you call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function.

## -struct-fields

### -field usri1025_code_page

Specifies a <b>DWORD</b> value that indicates the code page for the user's language of choice. The user is specified in the <i>username</i> parameter to the 
<b>NetUserSetInfo</b> function. 




This value is ignored.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>