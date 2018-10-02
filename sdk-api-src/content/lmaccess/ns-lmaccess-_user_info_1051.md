---
UID: NS:lmaccess._USER_INFO_1051
title: "_USER_INFO_1051"
author: windows-sdk-content
description: The USER_INFO_1051 structure contains the relative ID (RID) associated with the user account. This information level is valid only when you call the NetUserSetInfo function.
old-location: netmgmt\user_info_1051_str.htm
tech.root: NetMgmt
ms.assetid: dbd7c63b-c383-48dd-98f2-087f2b41fc52
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPUSER_INFO_1051, *PUSER_INFO_1051, LPUSER_INFO_1051, LPUSER_INFO_1051 structure pointer [Network Management], PUSER_INFO_1051, PUSER_INFO_1051 structure pointer [Network Management], USER_INFO_1051, USER_INFO_1051 structure [Network Management], _USER_INFO_1051, _win32_user_info_1051_str, lmaccess/LPUSER_INFO_1051, lmaccess/PUSER_INFO_1051, lmaccess/USER_INFO_1051, netmgmt.user_info_1051_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
---

# _USER_INFO_1051 structure


## -description


The
				<b>USER_INFO_1051</b> structure contains the relative ID (RID) associated with the user account. This information level is valid only when you call the 
<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> function.


## -struct-fields




### -field usri1051_primary_group_id

Specifies a <b>DWORD</b> value that contains the RID of the Primary Global Group for the user specified in the <i>username</i> parameter to the 
<b>NetUserSetInfo</b> function. This member must be the RID of a global group that represents the enrolled user. For more information about RIDs, see 
<a href="https://msdn.microsoft.com/528412e7-c2b6-4ddd-86de-999252972421">SID Components</a>.


## -see-also




<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/cf0e5102-3924-46c0-8124-0aa04e95f48d">User Functions</a>
 

 

