---
UID: NF:cscobj.IOfflineFilesItemFilter.GetTimeFilter
title: IOfflineFilesItemFilter::GetTimeFilter
author: windows-sdk-content
description: Provides time-value-comparison semantics to control filtering of items based on time.
old-location: of\iofflinefilesitemfilter_gettimefilter.htm
tech.root: OfflineFiles
ms.assetid: 397611e7-60e5-46d6-b90b-5aed7fff6a43
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetTimeFilter, GetTimeFilter method [Offline Files], GetTimeFilter method [Offline Files],IOfflineFilesItemFilter interface, IOfflineFilesItemFilter interface [Offline Files],GetTimeFilter method, IOfflineFilesItemFilter.GetTimeFilter, IOfflineFilesItemFilter::GetTimeFilter, cscobj/IOfflineFilesItemFilter::GetTimeFilter, of.iofflinefilesitemfilter_gettimefilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesItemFilter.GetTimeFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- cscobj.h
: 
- IOfflineFilesItemFilter.GetTimeFilter
: 
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

Receives an <a href="https://msdn.microsoft.com/en-us/library/Bb530647(v=VS.85).aspx">OFFLINEFILES_ITEM_TIME</a> enumeration value that indicates which time value associated with the cache item is to be used in the evaluation.

Only one value is to be provided.  This is not a mask.


### -param pCompare [out]

Receives an <a href="https://msdn.microsoft.com/en-us/library/Bb530643(v=VS.85).aspx">OFFLINEFILES_COMPARE</a> enumeration value that indicates the type of logical comparison to perform between the selected item time and the filter time pointed to by the <i>pftTime</i> parameter.


## -returns



Returns <b>S_OK</b> if the filter supports time filtering and the time filtering information is provided.

Returns <b>E_NOTIMPL</b> if time filtering is not supported.

Any other error value causes the creation of the enumerator to fail.




## -remarks



In these expressions, the item time is placed on the left side of the expression.  For example:

match = item_time &gt;= filter_time

This method may be implemented in any filter type (inclusion, exclusion) or filter target (file, container).




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530576(v=VS.85).aspx">IOfflineFilesItemFilter</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb530643(v=VS.85).aspx">OFFLINEFILES_COMPARE</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb530647(v=VS.85).aspx">OFFLINEFILES_ITEM_TIME</a>
 

 

