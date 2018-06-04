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

# WS_DURATION_COMPARISON_CALLBACK callback function


## -description


Compares two durations.
            A duration represents a unit of time as an eight-dimensional space where the coordinates designate the year, month, day, hour, minute, second, millisecond, and CPU tick as represented by the <a href="https://msdn.microsoft.com/ccb08c23-8c6f-4ea7-a43b-c30a0df75805">WS_DURATION</a> data structure.


## -parameters




### -param *duration1 [in]


                    A pointer to a <a href="https://msdn.microsoft.com/ccb08c23-8c6f-4ea7-a43b-c30a0df75805">WS_DURATION</a> structure representing the first duration to compare.
                


### -param *duration2 [in]


                    A  pointer to a <a href="https://msdn.microsoft.com/ccb08c23-8c6f-4ea7-a43b-c30a0df75805">WS_DURATION</a> structure representing the second duration.
                


### -param *result [out]


                    The relationship between the durations as one of the following values:
                    <ul>
<li>-1 if <i>duration1</i> is less than <i>duration2</i></li>
<li> 0 if <i>duration1</i> is equal to <i>duration2</i></li>
<li> 1 if <i>duration1</i> is greater than <i>duration2</i></li>
</ul>



### -param *error [in, optional]

A pointer to  a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> handle where additional error information should be stored if the function fails.
                


## -returns



This callback function does not return a value.




## -remarks




                If the function cannot compare the specified durations, it should return <b>WS_E_INVALID_FORMAT</b>. 
            (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)



