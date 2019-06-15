---
UID: NS:lmaccess._USER_INFO_1051
title: USER_INFO_1051 (lmaccess.h)
author: windows-sdk-content
description: The USER_INFO_1051 structure contains the relative ID (RID) associated with the user account. This information level is valid only when you call the NetUserSetInfo function.
old-location: netmgmt\user_info_1051_str.htm
tech.root: NetMgmt
ms.assetid: dbd7c63b-c383-48dd-98f2-087f2b41fc52
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPUSER_INFO_1051, *PUSER_INFO_1051, LPUSER_INFO_1051, LPUSER_INFO_1051 structure pointer [Network Management], PUSER_INFO_1051, PUSER_INFO_1051 structure pointer [Network Management], USER_INFO_1051, USER_INFO_1051 structure [Network Management], _win32_user_info_1051_str, lmaccess/LPUSER_INFO_1051, lmaccess/PUSER_INFO_1051, lmaccess/USER_INFO_1051, netmgmt.user_info_1051_str"
ms.topic: struct
f1_keywords: ["lmaccess/USER_INFO_1051"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - USER_INFO_1051
product: Windows
targetos: Windows
req.typenames: USER_INFO_1051, *PUSER_INFO_1051, *LPUSER_INFO_1051
req.redist: 
ms.custom: 19H1
---

# USER_INFO_1051 structure


## -description


The
				<b>USER_INFO_1051</b> structure contains the relative ID (RID) associated with the user account. This information level is valid only when you call the 
<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function.


## -struct-fields




### -field usri1051_primary_group_id

Specifies a <b>DWORD</b> value that contains the RID of the Primary Global Group for the user specified in the <i>username</i> parameter to the 
<b>NetUserSetInfo</b> function. This member must be the RID of a global group that represents the enrolled user. For more information about RIDs, see 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/sid-components">SID Components</a>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/user-functions">User Functions</a>
 

 

