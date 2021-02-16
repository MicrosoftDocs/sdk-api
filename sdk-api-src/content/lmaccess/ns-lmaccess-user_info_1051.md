---
UID: NS:lmaccess._USER_INFO_1051
title: USER_INFO_1051 (lmaccess.h)
description: The USER_INFO_1051 structure contains the relative ID (RID) associated with the user account. This information level is valid only when you call the NetUserSetInfo function.
helpviewer_keywords: ["*LPUSER_INFO_1051","*PUSER_INFO_1051","LPUSER_INFO_1051","LPUSER_INFO_1051 structure pointer [Network Management]","PUSER_INFO_1051","PUSER_INFO_1051 structure pointer [Network Management]","USER_INFO_1051","USER_INFO_1051 structure [Network Management]","_win32_user_info_1051_str","lmaccess/LPUSER_INFO_1051","lmaccess/PUSER_INFO_1051","lmaccess/USER_INFO_1051","netmgmt.user_info_1051_str"]
old-location: netmgmt\user_info_1051_str.htm
tech.root: NetMgmt
ms.assetid: dbd7c63b-c383-48dd-98f2-087f2b41fc52
ms.date: 12/05/2018
ms.keywords: '*LPUSER_INFO_1051, *PUSER_INFO_1051, LPUSER_INFO_1051, LPUSER_INFO_1051 structure pointer [Network Management], PUSER_INFO_1051, PUSER_INFO_1051 structure pointer [Network Management], USER_INFO_1051, USER_INFO_1051 structure [Network Management], _win32_user_info_1051_str, lmaccess/LPUSER_INFO_1051, lmaccess/PUSER_INFO_1051, lmaccess/USER_INFO_1051, netmgmt.user_info_1051_str'
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
req.typenames: USER_INFO_1051, *PUSER_INFO_1051, *LPUSER_INFO_1051
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_INFO_1051
 - lmaccess/_USER_INFO_1051
 - PUSER_INFO_1051
 - lmaccess/PUSER_INFO_1051
 - USER_INFO_1051
 - lmaccess/USER_INFO_1051
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
 - USER_INFO_1051
---

# USER_INFO_1051 structure


## -description

The
				<b>USER_INFO_1051</b> structure contains the relative ID (RID) associated with the user account. This information level is valid only when you call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function.

## -struct-fields

### -field usri1051_primary_group_id

Specifies a <b>DWORD</b> value that contains the RID of the Primary Global Group for the user specified in the <i>username</i> parameter to the 
<b>NetUserSetInfo</b> function. This member must be the RID of a global group that represents the enrolled user. For more information about RIDs, see 
<a href="/windows/desktop/SecAuthZ/sid-components">SID Components</a>.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>