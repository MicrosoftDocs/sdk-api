---
UID: NS:lmaccess._USER_INFO_10
title: USER_INFO_10 (lmaccess.h)
description: The USER_INFO_10 structure contains information about a user account, including the account name, comments associated with the account, and the user's full name.
helpviewer_keywords: ["*LPUSER_INFO_10","*PUSER_INFO_10","LPUSER_INFO_10","LPUSER_INFO_10 structure pointer [Network Management]","PUSER_INFO_10","PUSER_INFO_10 structure pointer [Network Management]","USER_INFO_10","USER_INFO_10 structure [Network Management]","_win32_user_info_10_str","lmaccess/LPUSER_INFO_10","lmaccess/PUSER_INFO_10","lmaccess/USER_INFO_10","netmgmt.user_info_10_str"]
old-location: netmgmt\user_info_10_str.htm
tech.root: NetMgmt
ms.assetid: f85e3e92-02b2-4ee8-8a82-38e4ef5b4072
ms.date: 12/05/2018
ms.keywords: '*LPUSER_INFO_10, *PUSER_INFO_10, LPUSER_INFO_10, LPUSER_INFO_10 structure pointer [Network Management], PUSER_INFO_10, PUSER_INFO_10 structure pointer [Network Management], USER_INFO_10, USER_INFO_10 structure [Network Management], _win32_user_info_10_str, lmaccess/LPUSER_INFO_10, lmaccess/PUSER_INFO_10, lmaccess/USER_INFO_10, netmgmt.user_info_10_str'
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
req.typenames: USER_INFO_10, *PUSER_INFO_10, *LPUSER_INFO_10
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_INFO_10
 - lmaccess/_USER_INFO_10
 - PUSER_INFO_10
 - lmaccess/PUSER_INFO_10
 - USER_INFO_10
 - lmaccess/USER_INFO_10
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
 - USER_INFO_10
---

# USER_INFO_10 structure


## -description

The
				<b>USER_INFO_10</b> structure contains information about a user account, including the account name, comments associated with the account, and the user's full name.

## -struct-fields

### -field usri10_name

Pointer to a Unicode string that specifies the name of the user account. Calls to the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function ignore this member. For more information, see the following Remarks section.

### -field usri10_comment

Pointer to a Unicode string that contains a comment associated with the user account. The string can be a null string, or can have any number of characters before the terminating null character.

### -field usri10_usr_comment

Pointer to a Unicode string that contains a user comment. This string can be a null string, or it can have any number of characters before the terminating null character.

### -field usri10_full_name

Pointer to a Unicode string that contains the full name of the user. This string can be a null string, or it can have any number of characters before the terminating null character.

## -remarks

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuserdel">NetUserDel</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuserenum">NetUserEnum</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>