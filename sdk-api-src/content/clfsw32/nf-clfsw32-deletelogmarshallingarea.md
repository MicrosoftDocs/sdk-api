---
UID: NF:clfsw32.DeleteLogMarshallingArea
title: DeleteLogMarshallingArea function (clfsw32.h)
description: Deletes a marshaling area that is created by a successful call to CreateLogMarshallingArea.
helpviewer_keywords: ["DeleteLogMarshallingArea","DeleteLogMarshallingArea function [Files]","clfsw32/DeleteLogMarshallingArea","fs.deletelogmarshalingarea","fs.deletelogmarshallingarea"]
old-location: fs\deletelogmarshallingarea.htm
tech.root: fs
ms.assetid: d58bd64f-fa76-4ab3-9660-e31e9029171c
ms.date: 12/05/2018
ms.keywords: DeleteLogMarshallingArea, DeleteLogMarshallingArea function [Files], clfsw32/DeleteLogMarshallingArea, fs.deletelogmarshalingarea, fs.deletelogmarshallingarea
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
 - DeleteLogMarshallingArea
 - clfsw32/DeleteLogMarshallingArea
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
 - DeleteLogMarshallingArea
---

# DeleteLogMarshallingArea function


## -description

Deletes a marshaling area that is created by a successful call to <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogmarshallingarea">CreateLogMarshallingArea</a>.

When you delete a marshaling area it does the following:<ul>
<li>Flushes the log to free pending log I/O blocks</li>
<li>Deallocates all log I/O blocks and invalidates all read contexts</li>
</ul>   The memory allocated by Common Log File System (CLFS)  to create the marshaling context is reclaimed when all read contexts are terminated.
<div class="alert"><b>Note</b>  Clients should not delete a marshaling area if there are pending  operations on the marshaling area.</div><div> </div>

## -parameters

### -param pvMarshal [in]

A pointer to the opaque marshaling context allocated by using the <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogmarshallingarea">CreateLogMarshallingArea</a> function.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following list identifies the possible  error codes:

## -see-also

<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogmarshallingarea">CreateLogMarshallingArea</a>