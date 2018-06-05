---
UID: NF:tapi.lineSetStatusMessages
title: lineSetStatusMessages function
author: windows-sdk-content
description: The lineSetStatusMessages function enables an application to specify which notification messages to receive for events related to status changes for the specified line or any of its addresses.
old-location: tapi2\linesetstatusmessages.htm
old-project: Tapi
ms.assetid: 08a93874-b0d5-4c00-b541-b51c312cfef6
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "_tapi2_linesetstatusmessages, lineSetStatusMessages, lineSetStatusMessages function [TAPI 2.2], tapi/lineSetStatusMessages, tapi2.linesetstatusmessages"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: FLICK_POINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Tapi32.dll
api_name:
-	lineSetStatusMessages
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
<a href="https://msdn.microsoft.com/41e8a777-a57a-4d6c-850f-e21b58081b0d">LINEDEVSTATE_ Constants</a>.


### -param dwAddressStates

Bit array that identifies for which address status changes a message is to be sent to the application. This parameter uses one or more of the 
<a href="https://msdn.microsoft.com/f06140d0-f41a-4228-93c5-21d609af5473">LINEADDRESSSTATE_ Constants</a>.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALADDRESSSTATE, LINEERR_OPERATIONFAILED, LINEERR_INVALLINEHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALLINESTATE, LINEERR_UNINITIALIZED, LINEERR_NOMEM, LINEERR_OPERATIONUNAVAIL.




## -remarks



TAPI defines a number of messages that notify applications about events occurring on lines and addresses. An application may not be interested in receiving all address and line status change messages. The 
<b>lineSetStatusMessages</b> function can be used to select which messages the application receives. By default, address and line status reporting is disabled.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/f254e331-d574-4fa7-8447-6e4535d3d773">LINE_CLOSE</a>



<a href="https://msdn.microsoft.com/15f616de-db47-4577-9a47-94f9292253dd">LINE_LINEDEVSTATE</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/4b406f19-be9b-4130-91a7-5fdfa56f7fc3">lineInitialize</a>



<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>



<a href="https://msdn.microsoft.com/7dd39866-0b3e-47be-8aa8-adfb66df6644">lineOpen</a>
 

 

