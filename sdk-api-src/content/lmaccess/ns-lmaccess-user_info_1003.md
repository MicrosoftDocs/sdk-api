---
UID: NS:lmaccess._USER_INFO_1003
title: USER_INFO_1003 (lmaccess.h)
description: The USER_INFO_1003 structure contains a user password. This information level is valid only when you call the NetUserSetInfo function.
helpviewer_keywords: ["*LPUSER_INFO_1003","*PUSER_INFO_1003","LPUSER_INFO_1003","LPUSER_INFO_1003 structure pointer [Network Management]","PUSER_INFO_1003","PUSER_INFO_1003 structure pointer [Network Management]","USER_INFO_1003","USER_INFO_1003 structure [Network Management]","_win32_user_info_1003_str","lmaccess/LPUSER_INFO_1003","lmaccess/PUSER_INFO_1003","lmaccess/USER_INFO_1003","netmgmt.user_info_1003_str"]
old-location: netmgmt\user_info_1003_str.htm
tech.root: NetMgmt
ms.assetid: ef1d1ecd-7226-4e4e-a0b3-ec096d3b1207
ms.date: 12/05/2018
ms.keywords: '*LPUSER_INFO_1003, *PUSER_INFO_1003, LPUSER_INFO_1003, LPUSER_INFO_1003 structure pointer [Network Management], PUSER_INFO_1003, PUSER_INFO_1003 structure pointer [Network Management], USER_INFO_1003, USER_INFO_1003 structure [Network Management], _win32_user_info_1003_str, lmaccess/LPUSER_INFO_1003, lmaccess/PUSER_INFO_1003, lmaccess/USER_INFO_1003, netmgmt.user_info_1003_str'
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
req.typenames: USER_INFO_1003, *PUSER_INFO_1003, *LPUSER_INFO_1003
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_INFO_1003
 - lmaccess/_USER_INFO_1003
 - PUSER_INFO_1003
 - lmaccess/PUSER_INFO_1003
 - USER_INFO_1003
 - lmaccess/USER_INFO_1003
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
 - USER_INFO_1003
---

# USER_INFO_1003 structure


## -description

The
				<b>USER_INFO_1003</b> structure contains a user password. This information level is valid only when you call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function.

## -struct-fields

### -field usri1003_password

Specifies a Unicode string that contains the password for the user account specified in the <i>username</i> parameter to the 
<b>NetUserSetInfo</b> function. The length cannot exceed PWLEN bytes.

## -remarks

By convention, the length of passwords is limited to LM20_PWLEN characters.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuserenum">NetUserEnum</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetinfo">NetUserGetInfo</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>