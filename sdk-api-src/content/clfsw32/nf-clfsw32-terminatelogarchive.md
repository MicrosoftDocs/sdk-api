---
UID: NF:clfsw32.TerminateLogArchive
title: TerminateLogArchive function (clfsw32.h)
description: Deallocates system resources that are allocated originally for a log archive context by PrepareLogArchive.
helpviewer_keywords: ["TerminateLogArchive","TerminateLogArchive function [Files]","clfsw32/TerminateLogArchive","fs.terminatelogarchive"]
old-location: fs\terminatelogarchive.htm
tech.root: fs
ms.assetid: 885356e1-f7c4-4f3f-98c3-fb9b1d339e22
ms.date: 12/05/2018
ms.keywords: TerminateLogArchive, TerminateLogArchive function [Files], clfsw32/TerminateLogArchive, fs.terminatelogarchive
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
 - TerminateLogArchive
 - clfsw32/TerminateLogArchive
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
 - TerminateLogArchive
---

# TerminateLogArchive function


## -description

Deallocates  system resources that are  allocated originally for  a log archive context by   <a href="/windows/desktop/api/clfsw32/nf-clfsw32-preparelogarchive">PrepareLogArchive</a>.

## -parameters

### -param pvArchiveContext [in]

The archive context that is obtained from <a href="/windows/desktop/api/clfsw32/nf-clfsw32-preparelogarchive">PrepareLogArchive</a>.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following  error code is possible:

## -remarks

Failure to call this function after archiving  completes  results in a resource leak.

## -see-also

<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-preparelogarchive">PrepareLogArchive</a>