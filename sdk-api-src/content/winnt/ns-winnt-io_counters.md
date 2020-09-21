---
UID: NS:winnt._IO_COUNTERS
title: IO_COUNTERS (winnt.h)
description: Contains I/O accounting information for a process or a job object.
helpviewer_keywords: ["*PIO_COUNTERS","IO_COUNTERS","IO_COUNTERS structure","PIO_COUNTERS","PIO_COUNTERS structure pointer","_IO_COUNTERS","_win32_io_counters_str","base.io_counters_str","winnt/IO_COUNTERS","winnt/PIO_COUNTERS"]
old-location: base\io_counters_str.htm
tech.root: backup
ms.assetid: 78729cbe-5256-4939-a7cc-c393662f8361
ms.date: 12/05/2018
ms.keywords: '*PIO_COUNTERS, IO_COUNTERS, IO_COUNTERS structure, PIO_COUNTERS, PIO_COUNTERS structure pointer, _IO_COUNTERS, _win32_io_counters_str, base.io_counters_str, winnt/IO_COUNTERS, winnt/PIO_COUNTERS'
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
targetos: Windows
req.typenames: IO_COUNTERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IO_COUNTERS
 - winnt/_IO_COUNTERS
 - IO_COUNTERS
 - winnt/IO_COUNTERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - IO_COUNTERS
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

<a href="/windows/desktop/api/winbase/nf-winbase-getprocessiocounters">GetProcessIoCounters</a>



<a href="/windows/win32/api/winnt/ns-winnt-jobobject_basic_and_io_accounting_information">JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION</a>