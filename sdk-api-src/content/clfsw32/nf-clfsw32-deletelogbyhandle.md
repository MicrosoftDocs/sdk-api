---
UID: NF:clfsw32.DeleteLogByHandle
title: DeleteLogByHandle function (clfsw32.h)
description: Marks the specified log for deletion. The log is actually deleted when all handles, marshaling areas, and read contexts to the log are closed. If the log is a physical log, its underlying containers are deleted.
helpviewer_keywords: ["DeleteLogByHandle","DeleteLogByHandle function [Files]","clfsw32/DeleteLogByHandle","fs.deletelogbyhandle"]
old-location: fs\deletelogbyhandle.htm
tech.root: fs
ms.assetid: 2426058f-312c-4946-ac12-52e55a3307b5
ms.date: 12/05/2018
ms.keywords: DeleteLogByHandle, DeleteLogByHandle function [Files], clfsw32/DeleteLogByHandle, fs.deletelogbyhandle
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
 - DeleteLogByHandle
 - clfsw32/DeleteLogByHandle
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
 - DeleteLogByHandle
---

# DeleteLogByHandle function


## -description

Marks the specified log for deletion. The log is actually deleted when all handles, marshaling areas, and read contexts to the log are closed.  If the log is a physical log, its underlying containers are deleted.

When a log is marked for deletion, requests to open new client log streams fail.
<div class="alert"><b>Note</b>  This function differs from <a href="/windows/desktop/api/clfsw32/nf-clfsw32-deletelogfile">DeleteLogFile</a>, because it takes a valid open handle to the log object instead of the log name.</div><div> </div>

## -parameters

### -param hLog [in]

A handle to an open log that is obtained by a successful call to <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a>. The log must have been created with DELETE access or you cannot delete the log.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following list identifies the possible error codes:

## -see-also

<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-deletelogfile">DeleteLogFile</a>