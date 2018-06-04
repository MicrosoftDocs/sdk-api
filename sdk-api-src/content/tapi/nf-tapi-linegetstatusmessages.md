---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
<a href="https://msdn.microsoft.com/08a93874-b0d5-4c00-b541-b51c312cfef6">lineSetStatusMessages</a>
		 function can be used to select which messages the application wants to receive. By default, address status and line status reporting is disabled.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/f254e331-d574-4fa7-8447-6e4535d3d773">LINE_CLOSE</a>



<a href="https://msdn.microsoft.com/15f616de-db47-4577-9a47-94f9292253dd">LINE_LINEDEVSTATE</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/08a93874-b0d5-4c00-b541-b51c312cfef6">lineSetStatusMessages</a>
 

 

