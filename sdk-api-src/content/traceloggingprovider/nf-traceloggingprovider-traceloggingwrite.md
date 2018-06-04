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

# TraceLoggingWrite macro


## -description


Emits an event.


## -parameters




### -param hProvider [in]

A provider registration handle.


### -param eventName [in]

The name of the event. This must be a string literal and not a variable. It cannot have any embedded nul characters values.


#### - args [in, optional]

Additional parameters added to the event. Up to 99 optional parameters may be specified. All parameters must be wrapper from <a href="https://msdn.microsoft.com/806F43F3-D376-4DBD-A4C5-B5F01E5D009D">TraceLogging Wrapper Macros</a>.


## -remarks




       You might get an error that a line is too long or the compiler is out of heap space when you submit optional parameters. This may occur because a line of code is longer than the maximum length allowed by the compiler. In this case, the parameters are too complex and you need to remove some from the macro to get it to work. 
     


       The maximum number of event data descriptors is 128. Since each parameter can have 0, 1, or 2, it is possible to hit the data descriptor limit before the argument limit. In addition, the maximum number of bytes per event is 65536, which includes headers, so actual maximum number may be less than this.
     


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>TraceLoggingWrite(
	g_hMyProvider,
	"MyEventName",
	TraceLoggingString(szValue1, "MyValue1"), // Field name MyValue1
	TraceLoggingInt32(value2, "MyValue2")); // Field name MyValue2
</pre>
</td>
</tr>
</table></span></div>


