---
UID: NF:clfsw32.TruncateLog
title: TruncateLog function (clfsw32.h)
description: Truncates the log. The function sets the end of the log to the specified value.
helpviewer_keywords: ["TruncateLog","TruncateLog function [Files]","clfsw32/TruncateLog","fs.truncatelog"]
old-location: fs\truncatelog.htm
tech.root: fs
ms.assetid: 76ef1a01-ba5c-4419-ac2f-4ba53dcc5bc4
ms.date: 12/05/2018
ms.keywords: TruncateLog, TruncateLog function [Files], clfsw32/TruncateLog, fs.truncatelog
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
 - TruncateLog
 - clfsw32/TruncateLog
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
 - TruncateLog
---

# TruncateLog function


## -description

Truncates the log. The function sets the end of the log to the specified value.

## -parameters

### -param pvMarshal [in]

A pointer to the opaque marshaling context that is allocated by calling the <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogmarshallingarea">CreateLogMarshallingArea</a> function.

### -param plsnEnd [in]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure that specifies the new end of a log.  

The LSN must be between the base log sequence number (LSN) of the log and the last LSN of the log.

### -param lpOverlapped [in, out, optional]

Reserved.  Set <i>Reserved</i> to <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following  list identifies the  possible error codes:

## -remarks

If the volume sector size is greater than 512 bytes, <b>TruncateLog</b> returns ERROR_NOT_SUPPORTED.

## -see-also

<a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a>



<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>