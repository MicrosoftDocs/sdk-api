---
UID: NF:clfsw32.SetEndOfLog
title: SetEndOfLog function (clfsw32.h)
description: This function has been deprecated. Use TruncateLog instead.
helpviewer_keywords: ["SetEndOfLog","SetEndOfLog function [Files]","clfsw32/SetEndOfLog","fs.setendoflog"]
old-location: fs\setendoflog.htm
tech.root: fs
ms.assetid: ef4f123f-3e1a-4082-93c7-f23783b1d45e
ms.date: 12/05/2018
ms.keywords: SetEndOfLog, SetEndOfLog function [Files], clfsw32/SetEndOfLog, fs.setendoflog
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
 - SetEndOfLog
 - clfsw32/SetEndOfLog
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
 - SetEndOfLog
---

# SetEndOfLog function


## -description

This function has been deprecated.  Use <a href="/windows/desktop/api/clfsw32/nf-clfsw32-truncatelog">TruncateLog</a> instead.

## -parameters

### -param hLog [in]

 A handle to the log that is obtained from <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a>.  

The log handle must refer to a dedicated log.

### -param plsnEnd [in]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure that specifies the new end of a log.  

The LSN must be between the base log sequence number (LSN) of the log and the last LSN of the log.

### -param lpOverlapped [in, out, optional]

Reserved.  Set <i>lpOverlapped</i> to <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following  list identifies the  possible error codes:

## -remarks

The <b>SetEndOfLog</b> function  truncates the log by setting the end of the log to the specified value.   This operation only works on dedicated logs.

<b>SetEndOfLog</b> can only be used to truncate a log.

## -see-also

<a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a>



<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>