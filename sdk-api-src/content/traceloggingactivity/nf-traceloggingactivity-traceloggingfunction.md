---
UID: NF:traceloggingactivity.TraceLoggingFunction
title: TraceLoggingFunction macro (traceloggingactivity.h)
author: windows-sdk-content
description: Creates a TraceLoggingThreadActivity named after the current function and writes a Start event for the activity. A Stop activity will be written at the end of the current scope.
old-location: tracelogging\traceloggingfunction.htm
tech.root: tracelogging
ms.assetid: 70382367-E0A0-4E5B-A14F-863BEC0615C5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TraceLoggingFunction, TraceLoggingFunction macro, tracelogging.traceloggingfunction, traceloggingactivity/TraceLoggingFunction
ms.topic: macro
f1_keywords: ["traceloggingactivity/TraceLoggingFunction"]
req.header: traceloggingactivity.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2012 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - traceloggingactivity.h
api_name:
 - TraceLoggingFunction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TraceLoggingFunction macro


## -description


Creates a <a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nl-traceloggingactivity-traceloggingthreadactivity~r1">TraceLoggingThreadActivity</a> named after the current function and writes a Start event for the activity. A Stop activity will be written at the end of the current scope.


## -parameters




### -param providerHandle [in]

A provider registration handle.


#### - args [in, optional]

Additional parameters that will be used to configure the activity’s Start event. Use <a href="https://docs.microsoft.com/windows/desktop/tracelogging/tracelogging-wrapper-macros">TraceLogging Wrapper Macros</a> to add values to the activity’s Start event or to configure the level/keyword of the activity’s Start and Stop events. The maximum number of optional parameters is 99. All parameters must be wrapper macros as defined in <b>TraceLogging Wrapper Macros</b>.


## -remarks



Invoke this macro at the beginning of a function to define an activity. This macro will then automatically create a <a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nl-traceloggingactivity-traceloggingthreadactivity~r1">TraceLoggingThreadActivity</a> object based on the name of the function, and start logging for the activity. It will also automatically generate and log a stop event when the function completes.
       

<div class="alert"><b>Caution</b>  <p class="note">Since this macro creates a <a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nl-traceloggingactivity-traceloggingthreadactivity~r1">TraceLoggingThreadActivity</a> object, you must ensure that no child activity will outlast the associated function, even in error cases or edge cases.
        

</div>
<div> </div>


