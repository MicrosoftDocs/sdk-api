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

# IOfflineFilesItemFilter::GetTimeFilter


## -description


Provides time-value-comparison semantics to control filtering of items based on time.


## -parameters




### -param pftTime [out]

Receives a pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure containing the UTC time value that the item is to be compared with.


### -param pbEvalTimeOfDay [out]

Receives a Boolean value indicating whether the time-of-day part of the <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> value is to be considered in the item evaluation.  If the flag value is <b>TRUE</b>, the time-of-day is considered.  If the flag value is <b>FALSE</b>, the time-of-day information is stripped from all time values involved in the evaluation; leaving only the year, month, and day.

This can be very helpful when the granularity of filtering is a day.


### -param pTimeType [out]

Receives an <a href="https://msdn.microsoft.com/14fd41fe-c5d9-4381-8ced-7ebe183fb30c">OFFLINEFILES_ITEM_TIME</a> enumeration value that indicates which time value associated with the cache item is to be used in the evaluation.

Only one value is to be provided.  This is not a mask.


### -param pCompare [out]

Receives an <a href="https://msdn.microsoft.com/17972c96-4ce1-43c0-bb6d-730787f0f93a">OFFLINEFILES_COMPARE</a> enumeration value that indicates the type of logical comparison to perform between the selected item time and the filter time pointed to by the <i>pftTime</i> parameter.


## -returns



Returns <b>S_OK</b> if the filter supports time filtering and the time filtering information is provided.

Returns <b>E_NOTIMPL</b> if time filtering is not supported.

Any other error value causes the creation of the enumerator to fail.




## -remarks



In these expressions, the item time is placed on the left side of the expression.  For example:

match = item_time &gt;= filter_time

This method may be implemented in any filter type (inclusion, exclusion) or filter target (file, container).




## -see-also




<a href="https://msdn.microsoft.com/e77b4f90-7a08-47f8-b297-8c1360167e1f">IOfflineFilesItemFilter</a>



<a href="https://msdn.microsoft.com/17972c96-4ce1-43c0-bb6d-730787f0f93a">OFFLINEFILES_COMPARE</a>



<a href="https://msdn.microsoft.com/14fd41fe-c5d9-4381-8ced-7ebe183fb30c">OFFLINEFILES_ITEM_TIME</a>
 

 

