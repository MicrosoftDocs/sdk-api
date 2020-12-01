---
UID: NF:clfsw32.CloseAndResetLogFile
title: CloseAndResetLogFile function (clfsw32.h)
description: Resets the log file and then shuts the log.
helpviewer_keywords: ["CloseAndResetLogFile","CloseAndResetLogFile function [Files]","clfsw32/CloseAndResetLogFile","fs.closeandresetlogfile"]
old-location: fs\closeandresetlogfile.htm
tech.root: fs
ms.assetid: 333b2de0-f472-43f7-ae57-5cefa7ab6746
ms.date: 12/05/2018
ms.keywords: CloseAndResetLogFile, CloseAndResetLogFile function [Files], clfsw32/CloseAndResetLogFile, fs.closeandresetlogfile
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
 - CloseAndResetLogFile
 - clfsw32/CloseAndResetLogFile
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
 - CloseAndResetLogFile
---

# CloseAndResetLogFile function


## -description

Resets the log file and then shuts the log.  This nullifies any client restart areas and resets the base log sequence number (LSN) for the log.   You do not need to close a log stream handle after calling this function.

## -parameters

### -param hLog [in]

A handle to a dedicated or multiplexed log. 

This handle is returned by a successful call to <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a>.  It is invalidated on successful completion of the call. No other operations that use this handle, or a derivative of this handle, can be called after this function has returned.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following  list identifies the possible error codes:

## -see-also

<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a>