---
UID: NS:lmaccess._USER_INFO_1024
title: USER_INFO_1024 (lmaccess.h)
description: The USER_INFO_1024 structure contains the country/region code for a network user's language of choice. This information level is valid only when you call the NetUserSetInfo function.
helpviewer_keywords: ["*LPUSER_INFO_1024","*PUSER_INFO_1024","LPUSER_INFO_1024","LPUSER_INFO_1024 structure pointer [Network Management]","PUSER_INFO_1024","PUSER_INFO_1024 structure pointer [Network Management]","USER_INFO_1024","USER_INFO_1024 structure [Network Management]","_win32_user_info_1024_str","lmaccess/LPUSER_INFO_1024","lmaccess/PUSER_INFO_1024","lmaccess/USER_INFO_1024","netmgmt.user_info_1024_str"]
old-location: netmgmt\user_info_1024_str.htm
tech.root: NetMgmt
ms.assetid: 8133238f-c968-4a65-a8dd-7b9a61a193f5
ms.date: 12/05/2018
ms.keywords: '*LPUSER_INFO_1024, *PUSER_INFO_1024, LPUSER_INFO_1024, LPUSER_INFO_1024 structure pointer [Network Management], PUSER_INFO_1024, PUSER_INFO_1024 structure pointer [Network Management], USER_INFO_1024, USER_INFO_1024 structure [Network Management], _win32_user_info_1024_str, lmaccess/LPUSER_INFO_1024, lmaccess/PUSER_INFO_1024, lmaccess/USER_INFO_1024, netmgmt.user_info_1024_str'
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
req.typenames: USER_INFO_1024, *PUSER_INFO_1024, *LPUSER_INFO_1024
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_INFO_1024
 - lmaccess/_USER_INFO_1024
 - PUSER_INFO_1024
 - lmaccess/PUSER_INFO_1024
 - USER_INFO_1024
 - lmaccess/USER_INFO_1024
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
 - USER_INFO_1024
---

# USER_INFO_1024 structure


## -description

The
				<b>USER_INFO_1024</b> structure contains the country/region code for a network user's language of choice. This information level is valid only when you call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function.

## -struct-fields

### -field usri1024_country_code

Specifies a <b>DWORD</b> value that indicates the country/region code for the user's language of choice. The user is specified in the <i>username</i> parameter to the 
<b>NetUserSetInfo</b> function. 




This value is ignored.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>