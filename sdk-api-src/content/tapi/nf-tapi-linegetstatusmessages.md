---
UID: NF:tapi.lineGetStatusMessages
title: lineGetStatusMessages function
author: windows-sdk-content
description: The lineGetStatusMessages function enables an application to query which notification messages the application is set up to receive for events related to status changes for the specified line or any of its addresses.
old-location: tapi2\linegetstatusmessages.htm
old-project: tapi
ms.assetid: c8ac3bff-be4f-43ca-9651-3263fa06af23
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: "_tapi2_linegetstatusmessages, lineGetStatusMessages, lineGetStatusMessages function [TAPI 2.2], tapi/lineGetStatusMessages, tapi2.linegetstatusmessages"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: FLICK_POINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineGetStatusMessages
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
<a href="https://msdn.microsoft.com/41e8a777-a57a-4d6c-850f-e21b58081b0d">LINEDEVSTATE_ Constants</a>.


### -param lpdwAddressStates

Bit array that identifies for which address status changes a message is to be sent to the application. If a flag is <b>TRUE</b>, that message is enabled; if <b>FALSE</b>, disabled. This parameter uses one or more of the 
<a href="https://msdn.microsoft.com/f06140d0-f41a-4228-93c5-21d609af5473">LINEADDRESSSTATE_ Constants</a>.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALLINEHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALPOINTER, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_UNINITIALIZED.




## -remarks



TAPI defines a number of messages that notify applications about events occurring on lines and addresses. An application may not be interested in receiving all address and line status change messages. The 
<a href="https://msdn.microsoft.com/08a93874-b0d5-4c00-b541-b51c312cfef6">lineSetStatusMessages</a>function can be used to select which messages the application wants to receive. By default, address status and line status reporting is disabled.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/f254e331-d574-4fa7-8447-6e4535d3d773">LINE_CLOSE</a>



<a href="https://msdn.microsoft.com/15f616de-db47-4577-9a47-94f9292253dd">LINE_LINEDEVSTATE</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/08a93874-b0d5-4c00-b541-b51c312cfef6">lineSetStatusMessages</a>
 

 

