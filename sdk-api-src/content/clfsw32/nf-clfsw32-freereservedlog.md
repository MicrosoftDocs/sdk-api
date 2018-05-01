---
UID: NF:clfsw32.FreeReservedLog
title: FreeReservedLog function
author: windows-driver-content
description: Reduces the number of reserved log records in a marshaling area made by calling ReserveAndAppendLog, ReserveAndAppendLogAligned, or AllocReservedLog.
old-location: fs\freereservedlog.htm
old-project: Clfs
ms.assetid: a5e71e4c-5871-4bea-a4a5-a56c7e70276b
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: FreeReservedLog, FreeReservedLog function [Files], clfsw32/FreeReservedLog, fs.freereservedlog
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clfsw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: LOG_MANAGEMENT_CALLBACKS, *PLOG_MANAGEMENT_CALLBACKS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Clfsw32.dll
api_name:
-	FreeReservedLog
product: Windows
targetos: Windows
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
---

# FreeReservedLog function


## -description


Reduces the number of reserved log records in a marshaling area made by calling <a href="https://msdn.microsoft.com/2036fc26-d040-4738-b66e-d5d3d0dbe385">ReserveAndAppendLog</a>, <a href="https://msdn.microsoft.com/fce678e3-3b30-4bb9-ab61-d7c8b24fd1d7">ReserveAndAppendLogAligned</a>, or <a href="https://msdn.microsoft.com/5e464b64-4617-4fbd-97cd-3c2db8f151b2">AllocReservedLog</a>.  By using this function, clients can free an aggregate set of records and bytes that are reserved in the marshaling area.


## -parameters




### -param pvMarshal [in, out]

A pointer to the opaque marshaling context that is allocated by using the <a href="https://msdn.microsoft.com/750c0615-bfac-402b-a590-6c9d800cf2d8">CreateLogMarshallingArea</a> function.


### -param cReservedRecords [in]

The number of reserved records to be freed.  

If the byte count of the adjustment in <i>pcbAdjustment</i> is positive,  <i>cReservedRecords</i> is the total  number of reserved records  that are remaining after the adjustment. Otherwise, this parameter specifies the number of records to be subtracted from the current number of reserved records, but can never exceed the reserved count.


### -param pcbAdjustment [in, out]

The number of bytes of reservation space affected by the adjustment.  

On input, if this number is positive,  it specifies the total remaining size of the reserved space after the adjustment. If this parameter  is negative,  its absolute value is  the number of bytes to be freed.

This value is usually an aggregate of the actual reserved space that is returned in a previous call to the following: 

<ul>
<li>
<a href="https://msdn.microsoft.com/2036fc26-d040-4738-b66e-d5d3d0dbe385">ReserveAndAppendLog</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fce678e3-3b30-4bb9-ab61-d7c8b24fd1d7">ReserveAndAppendLogAligned</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5e464b64-4617-4fbd-97cd-3c2db8f151b2">AllocReservedLog</a>
</li>
</ul>

## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following list identifies the  possible error codes:




## -remarks



When you reserve records, you reserve a specific size.  When you free those records, you must free the same size.




## -see-also




<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>
 

 

