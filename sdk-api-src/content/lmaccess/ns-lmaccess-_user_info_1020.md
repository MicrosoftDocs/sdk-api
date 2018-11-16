---
UID: NS:lmaccess._USER_INFO_1020
title: "_USER_INFO_1020"
author: windows-sdk-content
description: The USER_INFO_1020 structure contains the times during which a user can log on to the network. This information level is valid only when you call the NetUserSetInfo function.
old-location: netmgmt\user_info_1020_str.htm
tech.root: NetMgmt
ms.assetid: 959ed1f4-d5ee-4d77-abd7-bb681778f0b1
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*LPUSER_INFO_1020, *PUSER_INFO_1020, LPUSER_INFO_1020, LPUSER_INFO_1020 structure pointer [Network Management], PUSER_INFO_1020, PUSER_INFO_1020 structure pointer [Network Management], USER_INFO_1020, USER_INFO_1020 structure [Network Management], _USER_INFO_1020, _win32_user_info_1020_str, lmaccess/LPUSER_INFO_1020, lmaccess/PUSER_INFO_1020, lmaccess/USER_INFO_1020, netmgmt.user_info_1020_str"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - USER_INFO_1020
product: Windows
targetos: Windows
req.typenames: USER_INFO_1020, *PUSER_INFO_1020, *LPUSER_INFO_1020
req.redist: 
---

# _USER_INFO_1020 structure


## -description


The
				<b>USER_INFO_1020</b> structure contains the times during which a user can log on to the network. This information level is valid only when you call the 
<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> function.


## -struct-fields




### -field usri1020_units_per_week

Specifies a <b>DWORD</b> value that indicates the number of equal-length time units into which the week is divided. This value is required to compute the length of the bit string in the <b>usri1020_logon_hours</b> member. 




This value must be UNITS_PER_WEEK for LAN Manager 2.0. Calls to the 
<a href="https://msdn.microsoft.com/b5ca5f76-d40b-4abf-925a-0de54fc476e4">NetUserAdd</a> and 
<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> functions ignore this member.

For service applications, the units must be one of the following values: SAM_DAYS_PER_WEEK, SAM_HOURS_PER_WEEK, or SAM_MINUTES_PER_WEEK.


### -field usri1020_logon_hours

Pointer to a 21-byte (168 bits) bit string that specifies the times during which the user can log on. The user is specified in the <i>username</i> parameter to the 
<b>NetUserSetInfo</b> function. 




Each bit in the string represents a unique hour in the week, in Greenwich Mean Time (GMT). The first bit (bit 0, word 0) is Sunday, 0:00 to 0:59; the second bit (bit 1, word 0) is Sunday, 1:00 to 1:59; and so on. Note that bit 0 in word 0 represents Sunday from 0:00 to 0:59 only if you are in the GMT time zone. In all other cases you must adjust the bits according to your time zone offset (for example, GMT minus 8 hours for Pacific Standard Time).


## -see-also




<a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/cf0e5102-3924-46c0-8124-0aa04e95f48d">User Functions</a>
 

 

