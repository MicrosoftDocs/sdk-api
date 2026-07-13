---
UID: NF:tapi.lineSetStatusMessages
title: lineSetStatusMessages function (tapi.h)
description: The lineSetStatusMessages function enables an application to specify which notification messages to receive for events related to status changes for the specified line or any of its addresses.
helpviewer_keywords: ["_tapi2_linesetstatusmessages","lineSetStatusMessages","lineSetStatusMessages function [TAPI 2.2]","tapi/lineSetStatusMessages","tapi2.linesetstatusmessages"]
old-location: tapi2\linesetstatusmessages.htm
tech.root: tapi3
ms.assetid: 08a93874-b0d5-4c00-b541-b51c312cfef6
ms.date: 12/05/2018
ms.keywords: _tapi2_linesetstatusmessages, lineSetStatusMessages, lineSetStatusMessages function [TAPI 2.2], tapi/lineSetStatusMessages, tapi2.linesetstatusmessages
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
 - lineSetStatusMessages
 - tapi/lineSetStatusMessages
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ras-tapi32-l1-1-1.dll
 - Tapi32.dll
api_name:
 - lineSetStatusMessages
---

# lineSetStatusMessages function


## -description

The 
<b>lineSetStatusMessages</b> function enables an application to specify which notification messages to receive for events related to status changes for the specified line or any of its addresses.

## -parameters

### -param hLine

Handle to the line device.

### -param dwLineStates

Bit array that identifies for which line-device status changes a message is to be sent to the application. This parameter uses one or more of the 
<a href="/windows/desktop/Tapi/linedevstate--constants">LINEDEVSTATE_ Constants</a>.

### -param dwAddressStates

Bit array that identifies for which address status changes a message is to be sent to the application. This parameter uses one or more of the 
<a href="/windows/desktop/Tapi/lineaddressstate--constants">LINEADDRESSSTATE_ Constants</a>.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALADDRESSSTATE, LINEERR_OPERATIONFAILED, LINEERR_INVALLINEHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALLINESTATE, LINEERR_UNINITIALIZED, LINEERR_NOMEM, LINEERR_OPERATIONUNAVAIL.

## -remarks

TAPI defines a number of messages that notify applications about events occurring on lines and addresses. An application may not be interested in receiving all address and line status change messages. The 
<b>lineSetStatusMessages</b> function can be used to select which messages the application receives. By default, address and line status reporting is disabled.

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/Tapi/line-close">LINE_CLOSE</a>



<a href="/windows/desktop/Tapi/line-linedevstate">LINE_LINEDEVSTATE</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineinitialize">lineInitialize</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineopen">lineOpen</a>