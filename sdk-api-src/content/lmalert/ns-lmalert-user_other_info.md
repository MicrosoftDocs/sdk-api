---
UID: NS:lmalert._USER_OTHER_INFO
title: USER_OTHER_INFO (lmalert.h)
description: The USER_OTHER_INFO structure contains user error code information. The NetAlertRaise and NetAlertRaiseEx functions use the USER_OTHER_INFO structure to specify information about an event or condition of interest to a user.
helpviewer_keywords: ["*LPUSER_OTHER_INFO","*PUSER_OTHER_INFO","LPUSER_OTHER_INFO","LPUSER_OTHER_INFO structure pointer [Network Management]","PUSER_OTHER_INFO","PUSER_OTHER_INFO structure pointer [Network Management]","USER_OTHER_INFO","USER_OTHER_INFO structure [Network Management]","_win32_user_other_info_str","lmalert/LPUSER_OTHER_INFO","lmalert/PUSER_OTHER_INFO","lmalert/USER_OTHER_INFO","netmgmt.user_other_info_str"]
old-location: netmgmt\user_other_info_str.htm
tech.root: NetMgmt
ms.assetid: 2f6bd906-fdab-410a-8856-4482e047371f
ms.date: 12/05/2018
ms.keywords: '*LPUSER_OTHER_INFO, *PUSER_OTHER_INFO, LPUSER_OTHER_INFO, LPUSER_OTHER_INFO structure pointer [Network Management], PUSER_OTHER_INFO, PUSER_OTHER_INFO structure pointer [Network Management], USER_OTHER_INFO, USER_OTHER_INFO structure [Network Management], _win32_user_other_info_str, lmalert/LPUSER_OTHER_INFO, lmalert/PUSER_OTHER_INFO, lmalert/USER_OTHER_INFO, netmgmt.user_other_info_str'
req.header: lmalert.h
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
req.typenames: USER_OTHER_INFO, *PUSER_OTHER_INFO, *LPUSER_OTHER_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USER_OTHER_INFO
 - lmalert/_USER_OTHER_INFO
 - PUSER_OTHER_INFO
 - lmalert/PUSER_OTHER_INFO
 - USER_OTHER_INFO
 - lmalert/USER_OTHER_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmalert.h
api_name:
 - USER_OTHER_INFO
---

# USER_OTHER_INFO structure


## -description

The
				<b>USER_OTHER_INFO</b> structure contains user error code information. The 
<a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraise">NetAlertRaise</a> and 
<a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraiseex">NetAlertRaiseEx</a> functions use the 
<b>USER_OTHER_INFO</b> structure to specify information about an event or condition of interest to a user.

## -struct-fields

### -field alrtus_errcode

Specifies the error code for the new message in the message log.

### -field alrtus_numstrings

Specifies the number (0-9) of consecutive Unicode strings in the message log.

## -remarks

Additional variable-length data follows the 
<b>USER_OTHER_INFO</b> structure in the alert message buffer. The information is in the form of contiguous null-terminated character strings, as follows.

<table>
<tr>
<th>String</th>
<th>Meaning</th>
</tr>
<tr>
<td>username</td>
<td>The user who created the session.</td>
</tr>
<tr>
<td>computername</td>
<td>The computer that created the session.</td>
</tr>
</table>
 


<div> </div>


The calling application must allocate and free the memory for all structures and variable-length data in an alert message buffer.

See 
<a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraiseex">NetAlertRaiseEx</a> for a code sample that demonstrates how to raise a user alert.

## -see-also

<a href="/windows/desktop/api/lmalert/ns-lmalert-admin_other_info">ADMIN_OTHER_INFO</a>



<a href="/windows/desktop/NetMgmt/alert-functions">Alert Functions</a>



<a href="/windows/desktop/api/lmalert/ns-lmalert-errlog_other_info">ERRLOG_OTHER_INFO</a>



<a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraise">NetAlertRaise</a>



<a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraiseex">NetAlertRaiseEx</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/api/lmalert/ns-lmalert-print_other_info">PRINT_OTHER_INFO</a>



<a href="/windows/desktop/api/lmalert/ns-lmalert-std_alert">STD_ALERT</a>