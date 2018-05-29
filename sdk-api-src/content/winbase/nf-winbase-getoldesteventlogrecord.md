---
UID: NF:winbase.GetOldestEventLogRecord
title: GetOldestEventLogRecord function
author: windows-sdk-content
description: Retrieves the absolute record number of the oldest record in the specified event log.
old-location: base\getoldesteventlogrecord.htm
old-project: EventLog
ms.assetid: 2f64f82b-a5f5-4701-844b-5979a0124414
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetOldestEventLogRecord, GetOldestEventLogRecord function, _win32_getoldesteventlogrecord, base.getoldesteventlogrecord, winbase/GetOldestEventLogRecord
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
-	Ext-Ms-Win-AdvAPI32-EventLog-L1-1-1.dll
api_name:
-	GetOldestEventLogRecord
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetOldestEventLogRecord function


## -description


Retrieves the absolute record number of the oldest record in the specified event log.


## -parameters




### -param hEventLog [in]

A handle to the open event log. The 
<a href="https://msdn.microsoft.com/6cd8797a-aeaf-4603-b43c-b1ff45b6200a">OpenEventLog</a> or 
<a href="https://msdn.microsoft.com/cfef0912-9d35-44aa-a1d3-f9bb37213ce0">OpenBackupEventLog</a> function returns this handle.


### -param OldestRecord [out]

A pointer to a variable that receives the absolute record number of the oldest record in the specified event log.


## -returns




						If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The oldest record in an event log is not necessarily record number 1. For more information, see 
<a href="https://msdn.microsoft.com/73731505-97f5-4985-8d00-c6ce8604902d">Event Log Records</a>.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/e03d2ab5-50ea-4916-9774-850506714538">Querying for Event Information</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/fd5c12ec-3a3d-4b75-a573-0b27ae7a890b">Event Logging Functions</a>



<a href="https://msdn.microsoft.com/80cc8735-26a2-4ad3-a111-28f2c0c52e98">GetNumberOfEventLogRecords</a>



<a href="https://msdn.microsoft.com/cfef0912-9d35-44aa-a1d3-f9bb37213ce0">OpenBackupEventLog</a>



<a href="https://msdn.microsoft.com/6cd8797a-aeaf-4603-b43c-b1ff45b6200a">OpenEventLog</a>
 

 

