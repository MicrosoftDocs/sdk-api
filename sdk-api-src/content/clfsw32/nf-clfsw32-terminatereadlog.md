---
UID: NF:clfsw32.TerminateReadLog
title: TerminateReadLog function (clfsw32.h)
description: Terminates a read context. This function frees system-allocated resources associated with the specified read context. Do not attempt to read log records after calling this function; you will receive indeterminate results.
helpviewer_keywords: ["TerminateReadLog","TerminateReadLog function [Files]","clfsw32/TerminateReadLog","fs.terminatereadlog"]
old-location: fs\terminatereadlog.htm
tech.root: fs
ms.assetid: fb0a4c4e-cdb7-4c42-9102-bc76b8b70193
ms.date: 12/05/2018
ms.keywords: TerminateReadLog, TerminateReadLog function [Files], clfsw32/TerminateReadLog, fs.terminatereadlog
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
 - TerminateReadLog
 - clfsw32/TerminateReadLog
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
 - TerminateReadLog
---

# TerminateReadLog function


## -description

Terminates a read context. This function frees system-allocated resources associated with the specified read context. Do not attempt to read log records after calling this function; you will receive indeterminate results.

## -parameters

### -param pvCursorContext [in]

A pointer to a  read context that is returned by <a href="/windows/desktop/api/clfsw32/nf-clfsw32-readlogrecord">ReadLogRecord</a> or <a href="/windows/desktop/api/clfsw32/nf-clfsw32-readlogrestartarea">ReadLogRestartArea</a>.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following  list identifies the possible error codes:

## -remarks

It is important to deallocate unused read contexts.  Failure to call this function causes resource leaks.

## -see-also

<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-readlogrecord">ReadLogRecord</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-readlogrestartarea">ReadLogRestartArea</a>