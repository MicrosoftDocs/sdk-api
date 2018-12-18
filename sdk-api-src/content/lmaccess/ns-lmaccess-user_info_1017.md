---
UID: NS:lmaccess._USER_INFO_1017
title: USER_INFO_1017
author: windows-sdk-content
description: The USER_INFO_1017 structure contains expiration information for network user accounts. This information level is valid only when you call the NetUserSetInfo function.
old-location: netmgmt\user_info_1017_str.htm
tech.root: netmgmt
ms.assetid: 67ded50e-ab9a-4202-9496-1a39d1af0f58
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPUSER_INFO_1017, *PUSER_INFO_1017, LPUSER_INFO_1017, LPUSER_INFO_1017 structure pointer [Network Management], PUSER_INFO_1017, PUSER_INFO_1017 structure pointer [Network Management], USER_INFO_1017, USER_INFO_1017 structure [Network Management], _win32_user_info_1017_str, lmaccess/LPUSER_INFO_1017, lmaccess/PUSER_INFO_1017, lmaccess/USER_INFO_1017, netmgmt.user_info_1017_str"
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
 - USER_INFO_1017
product: Windows
targetos: Windows
req.typenames: USER_INFO_1017, *PUSER_INFO_1017, *LPUSER_INFO_1017
req.redist: 
---

# USER_INFO_1017 structure


## -description


The
				<b>USER_INFO_1017</b> structure contains expiration information for network user accounts. This information level is valid only when you call the 
<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> function.


## -struct-fields




### -field usri1017_acct_expires

Specifies a <b>DWORD</b> value that indicates when the user account expires. The user account is specified in the <i>username</i> parameter to the 
<b>NetUserSetInfo</b> function. 




The value is stored as the number of seconds that have elapsed since 00:00:00, January 1, 1970, GMT. Specify TIMEQ_FOREVER to indicate that the account never expires.


## -see-also




<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/cf0e5102-3924-46c0-8124-0aa04e95f48d">User Functions</a>
 

 

