---
UID: NF:clfsw32.GetLogFileInformation
title: GetLogFileInformation function (clfsw32.h)
description: Returns a buffer that contains metadata about a specified log and its current state, which is defined by the CLFS_INFORMATION structure.
helpviewer_keywords: ["GetLogFileInformation","GetLogFileInformation function [Files]","clfsw32/GetLogFileInformation","fs.getlogfileinformation"]
old-location: fs\getlogfileinformation.htm
tech.root: fs
ms.assetid: 29bb2f18-760d-4a38-8dce-85099da7f96c
ms.date: 12/05/2018
ms.keywords: GetLogFileInformation, GetLogFileInformation function [Files], clfsw32/GetLogFileInformation, fs.getlogfileinformation
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
 - GetLogFileInformation
 - clfsw32/GetLogFileInformation
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
 - GetLogFileInformation
---

# GetLogFileInformation function


## -description

Returns a buffer that contains metadata about a specified log and its current state, which is defined by the <a href="/windows/desktop/api/clfs/ns-clfs-cls_information">CLFS_INFORMATION</a> structure.

Data that is obtained  reflects the state of the log only at the time when the call is made. Typically, a client can continue to cache and use fields from this structure until the next time that it appends records or writes its restart area. At that time, some of the information becomes stale.

## -parameters

### -param hLog [in]

A handle to an open log that is obtained from a successful call to <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a>.  

The log handle can refer to a dedicated or multiplexed log.

### -param pinfoBuffer [in, out]

A pointer to a user-allocated <a href="/windows/desktop/api/clfs/ns-clfs-cls_information">CLFS_INFORMATION</a> structure that receives the log metadata.

### -param cbBuffer [in, out]

A pointer to a variable that on input specifies the size, in bytes, of the metadata buffer pointed to by <i>pinfoBuffer</i>.

 On output, it specifies the number of bytes that are actually copied into <i>pinfoBuffer</i>.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

 The following list identifies the possible error codes:

## -see-also

<a href="/windows/desktop/api/clfs/ns-clfs-cls_information">CLFS_INFORMATION</a>



<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a>



<a href="/previous-versions/windows/desktop/clfs/obtaining-the-next-lsn">Obtaining the Next LSN</a>