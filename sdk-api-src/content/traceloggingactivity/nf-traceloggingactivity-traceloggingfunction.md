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

# TraceLoggingFunction macro


## -description


Creates a <a href="https://msdn.microsoft.com/7666A28B-42B2-473F-852F-BD3F6CAA6AC7">TraceLoggingThreadActivity</a> named after the current function and writes a Start event for the activity. A Stop activity will be written at the end of the current scope.


## -parameters




### -param providerHandle

TBD


#### - args [in, optional]

Additional parameters that will be used to configure the activity’s Start event. Use <a href="https://msdn.microsoft.com/806F43F3-D376-4DBD-A4C5-B5F01E5D009D">TraceLogging Wrapper Macros</a> to add values to the activity’s Start event or to configure the level/keyword of the activity’s Start and Stop events. The maximum number of optional parameters is 99. All parameters must be wrapper macros as defined in <b>TraceLogging Wrapper Macros</b>.


#### - hProvider [in]

A provider registration handle.


## -remarks




         Invoke this macro at the beginning of a function to define an activity. This macro will then automatically create a <a href="https://msdn.microsoft.com/7666A28B-42B2-473F-852F-BD3F6CAA6AC7">TraceLoggingThreadActivity</a> object based on the name of the function, and start logging for the activity. It will also automatically generate and log a stop event when the function completes.
       

<div class="alert"><b>Caution</b>  <p class="note">
          Since this macro creates a <a href="https://msdn.microsoft.com/7666A28B-42B2-473F-852F-BD3F6CAA6AC7">TraceLoggingThreadActivity</a> object, you must ensure that no child activity will outlast the associated function, even in error cases or edge cases.
        

</div>
<div> </div>


