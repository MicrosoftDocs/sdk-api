---
UID: NS:lmaccess._USER_INFO_1007
title: USER_INFO_1007 (lmaccess.h)
description: The USER_INFO_1007 structure contains a comment associated with a user network account. This information level is valid only when you call the NetUserSetInfo function.
helpviewer_keywords: ["*LPUSER_INFO_1007","*PUSER_INFO_1007","LPUSER_INFO_1007","LPUSER_INFO_1007 structure pointer [Network Management]","PUSER_INFO_1007","PUSER_INFO_1007 structure pointer [Network Management]","USER_INFO_1007","USER_INFO_1007 structure [Network Management]","_win32_user_info_1007_str","lmaccess/LPUSER_INFO_1007","lmaccess/PUSER_INFO_1007","lmaccess/USER_INFO_1007","netmgmt.user_info_1007_str"]
old-location: netmgmt\user_info_1007_str.htm
tech.root: NetMgmt
ms.assetid: a2e49802-799d-4f98-aa6d-5cb1478cb4d4
ms.date: 12/05/2018
ms.keywords: '*LPUSER_INFO_1007, *PUSER_INFO_1007, LPUSER_INFO_1007, LPUSER_INFO_1007 structure pointer [Network Management], PUSER_INFO_1007, PUSER_INFO_1007 structure pointer [Network Management], USER_INFO_1007, USER_INFO_1007 structure [Network Management], _win32_user_info_1007_str, lmaccess/LPUSER_INFO_1007, lmaccess/PUSER_INFO_1007, lmaccess/USER_INFO_1007, netmgmt.user_info_1007_str'
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
req.typenames: USER_INFO_1007, *PUSER_INFO_1007, *LPUSER_INFO_1007
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_INFO_1007
 - lmaccess/_USER_INFO_1007
 - PUSER_INFO_1007
 - lmaccess/PUSER_INFO_1007
 - USER_INFO_1007
 - lmaccess/USER_INFO_1007
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
 - USER_INFO_1007
---

# USER_INFO_1007 structure


## -description

The
				<b>USER_INFO_1007</b> structure contains a comment associated with a user network account. This information level is valid only when you call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function.

## -struct-fields

### -field usri1007_comment

Pointer to a Unicode string that contains a comment to associate with the user account specified in the <i>username</i> parameter to the 
<b>NetUserSetInfo</b> function. This string can be a null string, or it can have any number of characters before the terminating null character.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>