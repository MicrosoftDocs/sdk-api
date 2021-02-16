---
UID: NS:lmalert._ADMIN_OTHER_INFO
title: ADMIN_OTHER_INFO (lmalert.h)
description: The ADMIN_OTHER_INFO structure contains error message information. The NetAlertRaise and NetAlertRaiseEx functions use the ADMIN_OTHER_INFO structure to specify information when raising an administrator's interrupting message.
helpviewer_keywords: ["*LPADMIN_OTHER_INFO","*PADMIN_OTHER_INFO","ADMIN_OTHER_INFO","ADMIN_OTHER_INFO structure [Network Management]","LPADMIN_OTHER_INFO","LPADMIN_OTHER_INFO structure pointer [Network Management]","PADMIN_OTHER_INFO","PADMIN_OTHER_INFO structure pointer [Network Management]","_win32_admin_other_info_str","lmalert/ADMIN_OTHER_INFO","lmalert/LPADMIN_OTHER_INFO","lmalert/PADMIN_OTHER_INFO","netmgmt.admin_other_info_str"]
old-location: netmgmt\admin_other_info_str.htm
tech.root: NetMgmt
ms.assetid: 43119dcf-7d04-4e3b-b1dc-20e814fbdc2f
ms.date: 12/05/2018
ms.keywords: '*LPADMIN_OTHER_INFO, *PADMIN_OTHER_INFO, ADMIN_OTHER_INFO, ADMIN_OTHER_INFO structure [Network Management], LPADMIN_OTHER_INFO, LPADMIN_OTHER_INFO structure pointer [Network Management], PADMIN_OTHER_INFO, PADMIN_OTHER_INFO structure pointer [Network Management], _win32_admin_other_info_str, lmalert/ADMIN_OTHER_INFO, lmalert/LPADMIN_OTHER_INFO, lmalert/PADMIN_OTHER_INFO, netmgmt.admin_other_info_str'
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
req.typenames: ADMIN_OTHER_INFO, *PADMIN_OTHER_INFO, *LPADMIN_OTHER_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ADMIN_OTHER_INFO
 - lmalert/_ADMIN_OTHER_INFO
 - PADMIN_OTHER_INFO
 - lmalert/PADMIN_OTHER_INFO
 - ADMIN_OTHER_INFO
 - lmalert/ADMIN_OTHER_INFO
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
 - ADMIN_OTHER_INFO
---

# ADMIN_OTHER_INFO structure


## -description

The
				<b>ADMIN_OTHER_INFO</b> structure contains error message information. The 
<a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraise">NetAlertRaise</a> and 
<a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraiseex">NetAlertRaiseEx</a> functions use the 
<b>ADMIN_OTHER_INFO</b> structure to specify information when raising an administrator's interrupting message.

## -struct-fields

### -field alrtad_errcode

Specifies the error code for the new message written to the message log.

### -field alrtad_numstrings

Specifies the number (0-9) of consecutive Unicode strings written to the message log.

## -remarks

Variable-length data follows the 
<b>ADMIN_OTHER_INFO</b> structure in the alert message buffer if you specify one or more strings in the <b>alrtad_numstrings</b> member. The calling application must allocate and free the memory for all structures and variable-length data in an alert message buffer.

See 
<a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraise">NetAlertRaise</a> and 
<a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraiseex">NetAlertRaiseEx</a> for code samples that demonstrate how to raise an administrative alert.

## -see-also

<a href="/windows/desktop/NetMgmt/alert-functions">Alert Functions</a>



<a href="/windows/desktop/api/lmalert/ns-lmalert-errlog_other_info">ERRLOG_OTHER_INFO</a>



<a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraise">NetAlertRaise</a>



<a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraiseex">NetAlertRaiseEx</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/api/lmalert/ns-lmalert-print_other_info">PRINT_OTHER_INFO</a>



<a href="/windows/desktop/api/lmalert/ns-lmalert-std_alert">STD_ALERT</a>



<a href="/windows/desktop/api/lmalert/ns-lmalert-user_other_info">USER_OTHER_INFO</a>