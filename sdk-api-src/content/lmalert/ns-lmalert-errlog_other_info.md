---
UID: NS:lmalert._ERRLOG_OTHER_INFO
title: ERRLOG_OTHER_INFO (lmalert.h)
description: The ERRLOG_OTHER_INFO structure contains error log information. The NetAlertRaise and NetAlertRaiseEx functions use the ERRLOG_OTHER_INFO structure to specify information when adding a new entry to the error log.
helpviewer_keywords: ["*LPERRLOG_OTHER_INFO","*PERRLOG_OTHER_INFO","ERRLOG_OTHER_INFO","ERRLOG_OTHER_INFO structure [Network Management]","LPERRLOG_OTHER_INFO","LPERRLOG_OTHER_INFO structure pointer [Network Management]","PERRLOG_OTHER_INFO","PERRLOG_OTHER_INFO structure pointer [Network Management]","_win32_errlog_other_info_str","lmalert/ERRLOG_OTHER_INFO","lmalert/LPERRLOG_OTHER_INFO","lmalert/PERRLOG_OTHER_INFO","netmgmt.errlog_other_info_str"]
old-location: netmgmt\errlog_other_info_str.htm
tech.root: NetMgmt
ms.assetid: 832ebe88-e1c4-4ce3-8057-922419b577f7
ms.date: 12/05/2018
ms.keywords: '*LPERRLOG_OTHER_INFO, *PERRLOG_OTHER_INFO, ERRLOG_OTHER_INFO, ERRLOG_OTHER_INFO structure [Network Management], LPERRLOG_OTHER_INFO, LPERRLOG_OTHER_INFO structure pointer [Network Management], PERRLOG_OTHER_INFO, PERRLOG_OTHER_INFO structure pointer [Network Management], _win32_errlog_other_info_str, lmalert/ERRLOG_OTHER_INFO, lmalert/LPERRLOG_OTHER_INFO, lmalert/PERRLOG_OTHER_INFO, netmgmt.errlog_other_info_str'
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
req.typenames: ERRLOG_OTHER_INFO, *PERRLOG_OTHER_INFO, *LPERRLOG_OTHER_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ERRLOG_OTHER_INFO
 - lmalert/_ERRLOG_OTHER_INFO
 - PERRLOG_OTHER_INFO
 - lmalert/PERRLOG_OTHER_INFO
 - ERRLOG_OTHER_INFO
 - lmalert/ERRLOG_OTHER_INFO
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
 - ERRLOG_OTHER_INFO
---

# ERRLOG_OTHER_INFO structure


## -description

The
				<b>ERRLOG_OTHER_INFO</b> structure contains error log information. The 
<a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraise">NetAlertRaise</a> and 
<a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraiseex">NetAlertRaiseEx</a> functions use the 
<b>ERRLOG_OTHER_INFO</b> structure to specify information when adding a new entry to the error log.

## -struct-fields

### -field alrter_errcode

Specifies the error code that was written to the error log.

### -field alrter_offset

Specifies the offset for the new entry in the error log.

## -remarks

The calling application must allocate and free the memory for all structures and variable-length data in an alert message buffer.

## -see-also

<a href="/windows/desktop/api/lmalert/ns-lmalert-admin_other_info">ADMIN_OTHER_INFO</a>



<a href="/windows/desktop/NetMgmt/alert-functions">Alert Functions</a>



<a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraise">NetAlertRaise</a>



<a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraiseex">NetAlertRaiseEx</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/api/lmalert/ns-lmalert-print_other_info">PRINT_OTHER_INFO</a>



<a href="/windows/desktop/api/lmalert/ns-lmalert-std_alert">STD_ALERT</a>



<a href="/windows/desktop/api/lmalert/ns-lmalert-user_other_info">USER_OTHER_INFO</a>