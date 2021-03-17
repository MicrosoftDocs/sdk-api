---
UID: NS:lmaccess._USER_INFO_1023
title: USER_INFO_1023 (lmaccess.h)
description: The USER_INFO_1023 structure contains the name of the server to which network logon requests should be sent. This information level is valid only when you call the NetUserSetInfo function.
helpviewer_keywords: ["*LPUSER_INFO_1023","*PUSER_INFO_1023","LPUSER_INFO_1023","LPUSER_INFO_1023 structure pointer [Network Management]","PUSER_INFO_1023","PUSER_INFO_1023 structure pointer [Network Management]","USER_INFO_1023","USER_INFO_1023 structure [Network Management]","_win32_user_info_1023_str","lmaccess/LPUSER_INFO_1023","lmaccess/PUSER_INFO_1023","lmaccess/USER_INFO_1023","netmgmt.user_info_1023_str"]
old-location: netmgmt\user_info_1023_str.htm
tech.root: NetMgmt
ms.assetid: 44985bbe-48d2-4fe9-9247-2800089269cb
ms.date: 12/05/2018
ms.keywords: '*LPUSER_INFO_1023, *PUSER_INFO_1023, LPUSER_INFO_1023, LPUSER_INFO_1023 structure pointer [Network Management], PUSER_INFO_1023, PUSER_INFO_1023 structure pointer [Network Management], USER_INFO_1023, USER_INFO_1023 structure [Network Management], _win32_user_info_1023_str, lmaccess/LPUSER_INFO_1023, lmaccess/PUSER_INFO_1023, lmaccess/USER_INFO_1023, netmgmt.user_info_1023_str'
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
req.typenames: USER_INFO_1023, *PUSER_INFO_1023, *LPUSER_INFO_1023
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_INFO_1023
 - lmaccess/_USER_INFO_1023
 - PUSER_INFO_1023
 - lmaccess/PUSER_INFO_1023
 - USER_INFO_1023
 - lmaccess/USER_INFO_1023
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
 - USER_INFO_1023
---

# USER_INFO_1023 structure


## -description

The
				<b>USER_INFO_1023</b> structure contains the name of the server to which network logon requests should be sent. This information level is valid only when you call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function.

## -struct-fields

### -field usri1023_logon_server

Pointer to a Unicode string that contains the name of the server to which logon requests for the user account should be sent. The user account is specified in the <i>username</i> parameter to the 
<b>NetUserSetInfo</b> function. 




Server names should be preceded by two backslashes (\\). To indicate that the logon request can be handled by any logon server, specify an asterisk (\\*) for the server name. A null string indicates that requests should be sent to the domain controller.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>