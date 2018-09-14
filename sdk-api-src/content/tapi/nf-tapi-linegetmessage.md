---
UID: NF:tapi.lineGetMessage
title: lineGetMessage function
author: windows-sdk-content
description: The lineGetMessage function returns the next TAPI message that is queued for delivery to an application that is using the Event Handle notification mechanism (see lineInitializeEx for further details).
old-location: tapi2\linegetmessage.htm
tech.root: TAPI
ms.assetid: ed6df53e-b01d-40bc-8676-b0f7e0eacfd1
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: "_tapi2_linegetmessage, lineGetMessage, lineGetMessage function [TAPI 2.2], tapi/lineGetMessage, tapi2.linegetmessage"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineGetMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineGetMessage function


## -description


The 
<b>lineGetMessage</b> function returns the next TAPI message that is queued for delivery to an application that is using the Event Handle notification mechanism (see 
<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a> for further details).


## -parameters




### -param hLineApp

Handle returned by 
<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>. The application must have set the LINEINITIALIZEEXOPTION_USEEVENT option in the <b>dwOptions</b> member of the 
<a href="https://msdn.microsoft.com/17fed282-6d08-4702-9ceb-9cbcc3737395">LINEINITIALIZEEXPARAMS</a> structure.


### -param lpMessage

Pointer to a 
<a href="https://msdn.microsoft.com/1d184948-4ba2-4c8c-8771-d1aea6c4f565">LINEMESSAGE</a> structure. Upon successful return from this function, the structure contains the next message that had been queued for delivery to the application.


### -param dwTimeout

Time-out interval, in milliseconds. The function returns if the interval elapses, even if no message can be returned. If <i>dwTimeout</i> is zero, the function checks for a queued message and returns immediately. If <i>dwTimeout</i> is INFINITE, the function's time-out interval never elapses.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALAPPHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALPOINTER, LINEERR_NOMEM.




## -remarks



If the 
<b>lineGetMessage</b> function has been called with a non-zero timeout and the application calls 
<a href="https://msdn.microsoft.com/d512508a-fb6a-41ec-a80d-f625abfdd184">lineShutdown</a> on another thread, this function returns immediately with LINEERR_INVALAPPHANDLE.

If the timeout expires (or was zero) and no message could be fetched from the queue, the function returns with the error LINEERR_OPERATIONFAILED.




## -see-also




<a href="https://msdn.microsoft.com/17fed282-6d08-4702-9ceb-9cbcc3737395">LINEINITIALIZEEXPARAMS</a>



<a href="https://msdn.microsoft.com/1d184948-4ba2-4c8c-8771-d1aea6c4f565">LINEMESSAGE</a>



<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>



<a href="https://msdn.microsoft.com/d512508a-fb6a-41ec-a80d-f625abfdd184">lineShutdown</a>
 

 

