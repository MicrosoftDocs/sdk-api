---
UID: NF:clfsw32.DeleteLogFile
title: DeleteLogFile function (clfsw32.h)
description: Marks a log for deletion. The log is actually deleted when all handles, marshaling areas, and read contexts to the log are closed. If the log is a physical log, its underlying containers are deleted.
helpviewer_keywords: ["DeleteLogFile","DeleteLogFile function [Files]","clfsw32/DeleteLogFile","fs.deletelogfile"]
old-location: fs\deletelogfile.htm
tech.root: fs
ms.assetid: a7dd8efc-b572-4591-9e46-1cd5105d4ca2
ms.date: 12/05/2018
ms.keywords: DeleteLogFile, DeleteLogFile function [Files], clfsw32/DeleteLogFile, fs.deletelogfile
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
 - DeleteLogFile
 - clfsw32/DeleteLogFile
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
 - DeleteLogFile
---

# DeleteLogFile function


## -description

Marks a log for deletion. The log is actually deleted when all handles, marshaling areas, and read contexts to the log are closed.  If the log is a physical log, its underlying containers are deleted.

When a log is marked for deletion, requests to open new client log streams fail. <div class="alert"><b>Note</b>  A closely related function is <a href="/windows/desktop/api/clfsw32/nf-clfsw32-deletelogbyhandle">DeleteLogByHandle</a>, which deletes a log when given the handle of the file.</div>
<div> </div>

## -parameters

### -param pszLogFileName [in]

The name of the log. 

This  name is specified when creating the log  by using  <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a>. The following example identifies the format  to use:

<b>log:&lt;</b><i>log name</i><b>&gt;[::&lt;</b><i>log stream name</i><b>&gt;]</b>

&lt;<i>log  name</i>&gt; corresponds to a valid file path in the  file system.

&lt;<i>log stream name</i>&gt; is the unique name of a log stream in the log.

  For more information, see <a href="/previous-versions/windows/desktop/clfs/log-types">Log Types</a>.

### -param pvReserved [in, optional]

This parameter is reserved and should be set to <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following list identifies the  possible error codes:

## -see-also

<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-deletelogbyhandle">DeleteLogByHandle</a>



<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>