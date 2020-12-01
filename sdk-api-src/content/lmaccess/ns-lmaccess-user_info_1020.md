---
UID: NS:lmaccess._USER_INFO_1020
title: USER_INFO_1020 (lmaccess.h)
description: The USER_INFO_1020 structure contains the times during which a user can log on to the network. This information level is valid only when you call the NetUserSetInfo function.
helpviewer_keywords: ["*LPUSER_INFO_1020","*PUSER_INFO_1020","LPUSER_INFO_1020","LPUSER_INFO_1020 structure pointer [Network Management]","PUSER_INFO_1020","PUSER_INFO_1020 structure pointer [Network Management]","USER_INFO_1020","USER_INFO_1020 structure [Network Management]","_win32_user_info_1020_str","lmaccess/LPUSER_INFO_1020","lmaccess/PUSER_INFO_1020","lmaccess/USER_INFO_1020","netmgmt.user_info_1020_str"]
old-location: netmgmt\user_info_1020_str.htm
tech.root: NetMgmt
ms.assetid: 959ed1f4-d5ee-4d77-abd7-bb681778f0b1
ms.date: 12/05/2018
ms.keywords: '*LPUSER_INFO_1020, *PUSER_INFO_1020, LPUSER_INFO_1020, LPUSER_INFO_1020 structure pointer [Network Management], PUSER_INFO_1020, PUSER_INFO_1020 structure pointer [Network Management], USER_INFO_1020, USER_INFO_1020 structure [Network Management], _win32_user_info_1020_str, lmaccess/LPUSER_INFO_1020, lmaccess/PUSER_INFO_1020, lmaccess/USER_INFO_1020, netmgmt.user_info_1020_str'
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
req.typenames: USER_INFO_1020, *PUSER_INFO_1020, *LPUSER_INFO_1020
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_INFO_1020
 - lmaccess/_USER_INFO_1020
 - PUSER_INFO_1020
 - lmaccess/PUSER_INFO_1020
 - USER_INFO_1020
 - lmaccess/USER_INFO_1020
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
 - USER_INFO_1020
---

# USER_INFO_1020 structure


## -description

The
				<b>USER_INFO_1020</b> structure contains the times during which a user can log on to the network. This information level is valid only when you call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> function.

## -struct-fields

### -field usri1020_units_per_week

Specifies a <b>DWORD</b> value that indicates the number of equal-length time units into which the week is divided. This value is required to compute the length of the bit string in the <b>usri1020_logon_hours</b> member. 




This value must be UNITS_PER_WEEK for LAN Manager 2.0. Calls to the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> and 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> functions ignore this member.

For service applications, the units must be one of the following values: SAM_DAYS_PER_WEEK, SAM_HOURS_PER_WEEK, or SAM_MINUTES_PER_WEEK.

### -field usri1020_logon_hours

Pointer to a 21-byte (168 bits) bit string that specifies the times during which the user can log on. The user is specified in the <i>username</i> parameter to the 
<b>NetUserSetInfo</b> function. 




Each bit in the string represents a unique hour in the week, in Greenwich Mean Time (GMT). The first bit (bit 0, word 0) is Sunday, 0:00 to 0:59; the second bit (bit 1, word 0) is Sunday, 1:00 to 1:59; and so on. Note that bit 0 in word 0 represents Sunday from 0:00 to 0:59 only if you are in the GMT time zone. In all other cases you must adjust the bits according to your time zone offset (for example, GMT minus 8 hours for Pacific Standard Time).

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/user-functions">User Functions</a>