---
UID: NF:clfsw32.FreeReservedLog
title: FreeReservedLog function (clfsw32.h)
description: Reduces the number of reserved log records in a marshaling area made by calling ReserveAndAppendLog, ReserveAndAppendLogAligned, or AllocReservedLog.
helpviewer_keywords: ["FreeReservedLog","FreeReservedLog function [Files]","clfsw32/FreeReservedLog","fs.freereservedlog"]
old-location: fs\freereservedlog.htm
tech.root: fs
ms.assetid: a5e71e4c-5871-4bea-a4a5-a56c7e70276b
ms.date: 12/05/2018
ms.keywords: FreeReservedLog, FreeReservedLog function [Files], clfsw32/FreeReservedLog, fs.freereservedlog
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
 - FreeReservedLog
 - clfsw32/FreeReservedLog
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
 - FreeReservedLog
---

# FreeReservedLog function


## -description

Reduces the number of reserved log records in a marshaling area made by calling <a href="/windows/desktop/api/clfsw32/nf-clfsw32-reserveandappendlog">ReserveAndAppendLog</a>, <a href="/windows/desktop/api/clfsw32/nf-clfsw32-reserveandappendlogaligned">ReserveAndAppendLogAligned</a>, or <a href="/windows/desktop/api/clfsw32/nf-clfsw32-allocreservedlog">AllocReservedLog</a>.  By using this function, clients can free an aggregate set of records and bytes that are reserved in the marshaling area.

## -parameters

### -param pvMarshal [in, out]

A pointer to the opaque marshaling context that is allocated by using the <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogmarshallingarea">CreateLogMarshallingArea</a> function.

### -param cReservedRecords [in]

The number of reserved records to be freed.  

If the byte count of the adjustment in <i>pcbAdjustment</i> is positive,  <i>cReservedRecords</i> is the total  number of reserved records  that are remaining after the adjustment. Otherwise, this parameter specifies the number of records to be subtracted from the current number of reserved records, but can never exceed the reserved count.

### -param pcbAdjustment [in, out]

The number of bytes of reservation space affected by the adjustment.  

On input, if this number is positive,  it specifies the total remaining size of the reserved space after the adjustment. If this parameter  is negative,  its absolute value is  the number of bytes to be freed.

This value is usually an aggregate of the actual reserved space that is returned in a previous call to the following: 

<ul>
<li>
<a href="/windows/desktop/api/clfsw32/nf-clfsw32-reserveandappendlog">ReserveAndAppendLog</a>
</li>
<li>
<a href="/windows/desktop/api/clfsw32/nf-clfsw32-reserveandappendlogaligned">ReserveAndAppendLogAligned</a>
</li>
<li>
<a href="/windows/desktop/api/clfsw32/nf-clfsw32-allocreservedlog">AllocReservedLog</a>
</li>
</ul>

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following list identifies the  possible error codes:

## -remarks

When you reserve records, you reserve a specific size.  When you free those records, you must free the same size.

## -see-also

<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>