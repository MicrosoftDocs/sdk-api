---
UID: NS:winnt._IO_COUNTERS
title: IO_COUNTERS (winnt.h)
author: windows-sdk-content
description: Contains I/O accounting information for a process or a job object.
old-location: base\io_counters_str.htm
tech.root: ProcThread
ms.assetid: 78729cbe-5256-4939-a7cc-c393662f8361
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PIO_COUNTERS, IO_COUNTERS, IO_COUNTERS structure, PIO_COUNTERS, PIO_COUNTERS structure pointer, _IO_COUNTERS, _win32_io_counters_str, base.io_counters_str, winnt/IO_COUNTERS, winnt/PIO_COUNTERS"
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - WinNT.h
api_name:
 - IO_COUNTERS
product: Windows
targetos: Windows
req.typenames: IO_COUNTERS
req.redist: 
---

# IO_COUNTERS structure


## -description


Contains I/O accounting information for a process or a job object. For a job object, the counters include all operations performed by all processes that have ever been associated with the job, in addition to all processes currently associated with the job.


## -struct-fields




### -field ReadOperationCount

The number of read operations performed.


### -field WriteOperationCount

The number of write operations performed.


### -field OtherOperationCount

The number of I/O operations performed, other than read and write operations.


### -field ReadTransferCount

The number of bytes read.


### -field WriteTransferCount

The number of bytes written.


### -field OtherTransferCount

The number of bytes transferred during operations other than read and write operations.


## -see-also




<a href="https://msdn.microsoft.com/e6973c1b-86bc-4fd1-aff6-26e87f8013c4">GetProcessIoCounters</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684144(v=VS.85).aspx">JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION</a>
 

 

