---
UID: NF:tapi.lineGetStatusMessages
title: lineGetStatusMessages function (tapi.h)
description: The lineGetStatusMessages function enables an application to query which notification messages the application is set up to receive for events related to status changes for the specified line or any of its addresses.
helpviewer_keywords: ["_tapi2_linegetstatusmessages","lineGetStatusMessages","lineGetStatusMessages function [TAPI 2.2]","tapi/lineGetStatusMessages","tapi2.linegetstatusmessages"]
old-location: tapi2\linegetstatusmessages.htm
tech.root: tapi3
ms.assetid: c8ac3bff-be4f-43ca-9651-3263fa06af23
ms.date: 12/05/2018
ms.keywords: _tapi2_linegetstatusmessages, lineGetStatusMessages, lineGetStatusMessages function [TAPI 2.2], tapi/lineGetStatusMessages, tapi2.linegetstatusmessages
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineGetStatusMessages
 - tapi/lineGetStatusMessages
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineGetStatusMessages
---

# lineGetStatusMessages function


## -description

The 
<b>lineGetStatusMessages</b> function enables an application to query which notification messages the application is set up to receive for events related to status changes for the specified line or any of its addresses.

## -parameters

### -param hLine

Handle to the line device.

### -param lpdwLineStates

Bit array that identifies for which line device status changes a message is to be sent to the application. If a flag is <b>TRUE</b>, that message is enabled; if <b>FALSE</b>, it is disabled. This parameter uses one or more of the 
<a href="/windows/desktop/Tapi/linedevstate--constants">LINEDEVSTATE_ Constants</a>.

### -param lpdwAddressStates

Bit array that identifies for which address status changes a message is to be sent to the application. If a flag is <b>TRUE</b>, that message is enabled; if <b>FALSE</b>, disabled. This parameter uses one or more of the 
<a href="/windows/desktop/Tapi/lineaddressstate--constants">LINEADDRESSSTATE_ Constants</a>.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALLINEHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALPOINTER, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_UNINITIALIZED.

## -remarks

TAPI defines a number of messages that notify applications about events occurring on lines and addresses. An application may not be interested in receiving all address and line status change messages. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetstatusmessages">lineSetStatusMessages</a> function can be used to select which messages the application wants to receive. By default, address status and line status reporting is disabled.

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/Tapi/line-close">LINE_CLOSE</a>



<a href="/windows/desktop/Tapi/line-linedevstate">LINE_LINEDEVSTATE</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetstatusmessages">lineSetStatusMessages</a>