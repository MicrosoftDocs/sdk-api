---
UID: NF:traceloggingprovider.TraceLoggingWrite
title: TraceLoggingWrite macro (traceloggingprovider.h)
description: Emits an event.
old-location: tracelogging\traceloggingwrite.htm
tech.root: tracelogging
ms.assetid: BFBC6802-64DC-478E-B09D-F550135994AB
ms.date: 12/05/2018
ms.keywords: TraceLoggingWrite, TraceLoggingWrite macro, tracelogging.traceloggingwrite, traceloggingprovider/TraceLoggingWrite
ms.topic: macro
f1_keywords:
- traceloggingprovider/TraceLoggingWrite
dev_langs:
- c++
req.header: traceloggingprovider.h
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
- traceloggingprovider.h
api_name:
- TraceLoggingWrite
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TraceLoggingWrite macro


## -description


Emits an event.


## -parameters




### -param hProvider [in]

A provider registration handle.


### -param eventName [in]

The name of the event. This must be a string literal and not a variable. It cannot have any embedded nul characters values.


#### - args [in, optional]

Additional parameters added to the event. Up to 99 optional parameters may be specified. All parameters must be wrapper from <a href="https://docs.microsoft.com/windows/desktop/tracelogging/tracelogging-wrapper-macros">TraceLogging Wrapper Macros</a>.


## -remarks



You might get an error that a line is too long or the compiler is out of heap space when you submit optional parameters. This may occur because a line of code is longer than the maximum length allowed by the compiler. In this case, the parameters are too complex and you need to remove some from the macro to get it to work. 
     

The maximum number of event data descriptors is 128. Since each parameter can have 0, 1, or 2, it is possible to hit the data descriptor limit before the argument limit. In addition, the maximum number of bytes per event is 65536, which includes headers, so actual maximum number may be less than this.
     


#### Examples


```cpp
TraceLoggingWrite(
	g_hMyProvider,
	"MyEventName",
	TraceLoggingString(szValue1, "MyValue1"), // Field name MyValue1
	TraceLoggingInt32(value2, "MyValue2")); // Field name MyValue2

```




