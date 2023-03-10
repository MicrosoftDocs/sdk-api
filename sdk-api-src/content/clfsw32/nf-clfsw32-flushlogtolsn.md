---
UID: NF:clfsw32.FlushLogToLsn
title: FlushLogToLsn function (clfsw32.h)
description: Forces all records appended to this marshaling area up to the record with the specified log sequence number (LSN) to be flushed to the disk. More records than specified may be flushed during this operation.
helpviewer_keywords: ["FlushLogToLsn","FlushLogToLsn function [Files]","clfsw32/FlushLogToLsn","fs.flushlogtolsn"]
old-location: fs\flushlogtolsn.htm
tech.root: fs
ms.assetid: d2a30ce1-e9c7-4dcf-b5fb-4355c9134461
ms.date: 12/05/2018
ms.keywords: FlushLogToLsn, FlushLogToLsn function [Files], clfsw32/FlushLogToLsn, fs.flushlogtolsn
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
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FlushLogToLsn
 - clfsw32/FlushLogToLsn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - FlushLogToLsn
---

# FlushLogToLsn function


## -description

Forces all records appended to this marshaling area up to the record with the specified log sequence number (LSN) to be flushed to the disk.  More records than specified may be flushed during this operation.

## -parameters

### -param pvMarshalContext [in]

A pointer to the  marshaling context that is allocated by using the <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogmarshallingarea">CreateLogMarshallingArea</a> function.

### -param plsnFlush [in]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure that specifies the LSN that is used to determine which records to flush.   

Specify CLFS_LSN_NULL to flush all records in the marshaling area.

### -param plsnLastFlushed [out, optional]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure. 

The LSN returned is greater than the LSN of any record flushed.  If the function  succeeds, the value of the LSN is never less than <i>plsnFlush</i>.  This value  is meaningful only  when  the function succeeds.

### -param pOverlapped [in, out, optional]

A pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that  is required for asynchronous operation. 

This parameter can be <b>NULL</b>  except for an asynchronous operation.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following list identifies the   possible error codes:

## -see-also

<a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a>



<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>