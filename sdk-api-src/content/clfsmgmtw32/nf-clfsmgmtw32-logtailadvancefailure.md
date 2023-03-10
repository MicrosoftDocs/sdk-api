---
UID: NF:clfsmgmtw32.LogTailAdvanceFailure
title: LogTailAdvanceFailure function (clfsmgmtw32.h)
description: The LogTailAdvanceFailure function is called by a log client to indicate that it cannot comply with a request from log management to advance its tail.
helpviewer_keywords: ["LogTailAdvanceFailure","LogTailAdvanceFailure function [Files]","clfsmgmtw32/LogTailAdvanceFailure","fs.logtailadvancefailure"]
old-location: fs\logtailadvancefailure.htm
tech.root: fs
ms.assetid: 4f57f7c9-e54b-4e64-a3d7-53e6f3d7ec98
ms.date: 12/05/2018
ms.keywords: LogTailAdvanceFailure, LogTailAdvanceFailure function [Files], clfsmgmtw32/LogTailAdvanceFailure, fs.logtailadvancefailure
req.header: clfsmgmtw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ClfsW32.lib
req.dll: ClfsW32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LogTailAdvanceFailure
 - clfsmgmtw32/LogTailAdvanceFailure
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClfsW32.dll
api_name:
 - LogTailAdvanceFailure
---

# LogTailAdvanceFailure function


## -description

The <b>LogTailAdvanceFailure</b> function is 
    called by a log client to indicate that it cannot comply with a request from log management to advance its 
    tail.

## -parameters

### -param hLog [in]

A handle to the log on which to resolve the log full condition.

### -param dwReason [in]

Win32 error code with the reason for the failure For a list of possible values, see 
      <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -returns

If the function succeeds, the return value is nonzero.
      

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Valid values include the following:

## -see-also

<a href="/previous-versions/windows/desktop/clfs/clfs-management-functions">CLFS Management Functions</a>