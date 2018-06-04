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

# EventEnabled function


## -description


Determines if the event is enabled for any session.


## -parameters




### -param RegHandle [in]

Registration handle of the provider. The handle comes from 
      <a href="https://msdn.microsoft.com/6025c3a6-7d88-49dc-bbc3-655c172dde3c">EventRegister</a>.

<div class="alert"><b>Note</b>  A valid registration handle 
      must be used.</div>
<div> </div>

### -param EventDescriptor [in]

Describes the event. For details, see <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>. 


## -returns



Returns <b>TRUE</b> if the event is enabled for a session; otherwise, <b>FALSE</b>.




## -remarks



Typically, providers do not call this function to determine if a session is expecting this event, they simply 
    write the event and ETW determines if the event is logged to the session. 

Providers may want to call this function if they need to perform extra work to generate the event. Calling 
    this function first to determine if a session is expecting this event or not, may save resources and time.

The provider would call this function if the provider generated an 
    <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a> structure for the event from the 
    manifest. If the event descriptor is not available, call the 
    <a href="https://msdn.microsoft.com/84c035b1-cdc7-47b7-b887-e5b508f17266">EventProviderEnabled</a> function.




## -see-also




<a href="https://msdn.microsoft.com/84c035b1-cdc7-47b7-b887-e5b508f17266">EventProviderEnabled</a>
 

 

