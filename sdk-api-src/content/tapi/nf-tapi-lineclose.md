---
UID: NF:tapi.lineClose
title: lineClose function (tapi.h)
description: The lineClose function closes the specified open line device.
helpviewer_keywords: ["_tapi2_lineclose","lineClose","lineClose function [TAPI 2.2]","tapi/lineClose","tapi2.lineclose"]
old-location: tapi2\lineclose.htm
tech.root: tapi3
ms.assetid: ec47a351-c693-4e71-bf23-c31110ca90a1
ms.date: 12/05/2018
ms.keywords: _tapi2_lineclose, lineClose, lineClose function [TAPI 2.2], tapi/lineClose, tapi2.lineclose
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
 - lineClose
 - tapi/lineClose
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
 - lineClose
---

# lineClose function


## -description

The 
<b>lineClose</b> function closes the specified open line device.

## -parameters

### -param hLine

Handle to the open line device to be closed. After the line has been successfully closed, this handle is no longer valid.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALLINEHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_UNINITIALIZED, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL.

## -remarks

If an application calls 
<b>lineClose</b> while it still has active calls on the opened line, the application's ownership of these calls is revoked. If the application was the sole owner of these calls, the calls are dropped as well. It is good programming practice for an application to dispose of the calls it owns on an opened line by explicitly relinquishing ownership and/or by dropping these calls prior to closing the line.

If the line was closed successfully, a 
<a href="/windows/desktop/Tapi/line-linedevstate">LINE_LINEDEVSTATE</a> message is sent to all applications that are monitoring the line status of open/close changes. Outstanding asynchronous replies are suppressed.

Service providers may find it useful or necessary to forcibly reclaim line devices from an application that has the line open. This can be useful to prevent an application from monopolizing the line device for too long. If this happens, a LINE_CLOSE message is sent to the application, specifying the line handle of the line device that was closed.

The 
<a href="/windows/desktop/api/tapi/nf-tapi-lineopen">lineOpen</a> function allocates resources to the invoking application, and applications can be prevented from opening a line if resources are unavailable. Therefore, an application that only occasionally uses a line device (such as for making outgoing calls) should close the line to free resources and allow other applications to open the line.

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/Tapi/line-close">LINE_CLOSE</a>



<a href="/windows/desktop/Tapi/line-linedevstate">LINE_LINEDEVSTATE</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineopen">lineOpen</a>