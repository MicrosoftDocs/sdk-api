---
UID: NC:webservices.WS_DURATION_COMPARISON_CALLBACK
title: WS_DURATION_COMPARISON_CALLBACK
author: windows-sdk-content
description: Compares two durations.
old-location: wsw\ws_duration_comparison_callback.htm
tech.root: wsw
ms.assetid: 69f5d387-15b1-41cc-a0f8-047b8f6adb93
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WS_DURATION_COMPARISON_CALLBACK, WS_DURATION_COMPARISON_CALLBACK callback, WS_DURATION_COMPARISON_CALLBACK callback function [Web Services for Windows], webservices/WS_DURATION_COMPARISON_CALLBACK, wsw.ws_duration_comparison_callback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_DURATION_COMPARISON_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WS_DURATION_COMPARISON_CALLBACK callback function


## -description


Compares two durations.A duration represents a unit of time as an eight-dimensional space where the coordinates designate the year, month, day, hour, minute, second, millisecond, and CPU tick as represented by the <a href="https://msdn.microsoft.com/ccb08c23-8c6f-4ea7-a43b-c30a0df75805">WS_DURATION</a> data structure.


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



