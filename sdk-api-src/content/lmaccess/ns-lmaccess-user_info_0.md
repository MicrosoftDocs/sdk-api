---
UID: NS:lmaccess._USER_INFO_0
title: USER_INFO_0 (lmaccess.h)
description: The USER_INFO_0 structure contains a user account name.
helpviewer_keywords: ["*LPUSER_INFO_0","*PUSER_INFO_0","LPUSER_INFO_0","LPUSER_INFO_0 structure pointer [Network Management]","PUSER_INFO_0","PUSER_INFO_0 structure pointer [Network Management]","USER_INFO_0","USER_INFO_0 structure [Network Management]","_win32_user_info_0_str","lmaccess/LPUSER_INFO_0","lmaccess/PUSER_INFO_0","lmaccess/USER_INFO_0","netmgmt.user_info_0_str"]
old-location: netmgmt\user_info_0_str.htm
tech.root: NetMgmt
ms.assetid: 5d24a2dd-d1ee-4c97-8fbc-0b336313b60c
ms.date: 12/05/2018
ms.keywords: '*LPUSER_INFO_0, *PUSER_INFO_0, LPUSER_INFO_0, LPUSER_INFO_0 structure pointer [Network Management], PUSER_INFO_0, PUSER_INFO_0 structure pointer [Network Management], USER_INFO_0, USER_INFO_0 structure [Network Management], _win32_user_info_0_str, lmaccess/LPUSER_INFO_0, lmaccess/PUSER_INFO_0, lmaccess/USER_INFO_0, netmgmt.user_info_0_str'
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
req.typenames: USER_INFO_0, *PUSER_INFO_0, *LPUSER_INFO_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_INFO_0
 - lmaccess/_USER_INFO_0
 - PUSER_INFO_0
 - lmaccess/PUSER_INFO_0
 - USER_INFO_0
 - lmaccess/USER_INFO_0
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
 - USER_INFO_0
---

# USER_INFO_0 structure


## -description

The
				<b>USER_INFO_0</b> structure contains a user account name.

## -struct-fields

### -field usri0_name

Pointer to a Unicode string that specifies the name of the user account. For the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function, this member specifies the name of the user.

## -remarks

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

## -see-also

<a href="/windows/desktop/api/lmuse/nf-lmuse-netusedel">NetUseDel</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuserenum">NetUserEnum</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>