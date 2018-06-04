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

# phoneGetMessage function


## -description


The 
<b>phoneGetMessage</b> function returns the next TAPI message that is queued for delivery to an application that is using the Event Handle notification mechanism (see 
<a href="https://msdn.microsoft.com/362e37df-4b14-4651-8d23-b70613e354c8">phoneInitializeEx</a> for further details).


## -parameters




### -param hPhoneApp

Handle returned by 
<a href="https://msdn.microsoft.com/362e37df-4b14-4651-8d23-b70613e354c8">phoneInitializeEx</a>. The application must have set the PHONEINITIALIZEEXOPTION_USEEVENT option in the <b>dwOptions</b> member of the 
<a href="https://msdn.microsoft.com/465653e4-b88a-42a0-99b0-ce26eeaf99fd">PHONEINITIALIZEEXPARAMS</a> structure.


### -param lpMessage

Pointer to a 
<a href="https://msdn.microsoft.com/3655efef-d24c-4d67-b1dc-29d1948a1869">PHONEMESSAGE</a> structure. Upon successful return from this function, the structure contains the next message that had been queued for delivery to the application.


### -param dwTimeout

Time-out interval, in milliseconds. The function returns if the interval elapses, even if no message can be returned. If <i>dwTimeout</i> is zero, the function checks for a queued message and returns immediately. If <i>dwTimeout</i> is INFINITE, the function's time-out interval never elapses.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALAPPHANDLE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPOINTER, PHONEERR_NOMEM.




## -remarks



If this function has been called with a nonzero timeout and the application calls 
<a href="https://msdn.microsoft.com/0cf8bc07-946a-450d-8062-b9e19c22a4c5">phoneShutdown</a> on another thread, this function returns immediately with PHONEERR_INVALAPPHANDLE.

If the timeout expires (or was zero) and no message could be fetched from the queue, the function returns with the error PHONEERR_OPERATIONFAILED.




## -see-also




<a href="https://msdn.microsoft.com/465653e4-b88a-42a0-99b0-ce26eeaf99fd">PHONEINITIALIZEEXPARAMS</a>



<a href="https://msdn.microsoft.com/3655efef-d24c-4d67-b1dc-29d1948a1869">PHONEMESSAGE</a>



<a href="https://msdn.microsoft.com/362e37df-4b14-4651-8d23-b70613e354c8">phoneInitializeEx</a>



<a href="https://msdn.microsoft.com/0cf8bc07-946a-450d-8062-b9e19c22a4c5">phoneShutdown</a>
 

 

