---
UID: NF:clfsw32.TruncateLog
title: TruncateLog function (clfsw32.h)
author: windows-sdk-content
description: Truncates the log. The function sets the end of the log to the specified value.
old-location: fs\truncatelog.htm
tech.root: Clfs
ms.assetid: 76ef1a01-ba5c-4419-ac2f-4ba53dcc5bc4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TruncateLog, TruncateLog function [Files], clfsw32/TruncateLog, fs.truncatelog
ms.topic: function
f1_keywords: 
 - "clfsw32/TruncateLog"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - TruncateLog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TruncateLog function


## -description


Truncates the log. The function sets the end of the log to the specified value.


## -parameters




### -param pvMarshal [in]

A pointer to the opaque marshaling context that is allocated by calling the <a href="https://docs.microsoft.com/windows/desktop/api/clfsw32/nf-clfsw32-createlogmarshallingarea">CreateLogMarshallingArea</a> function.


### -param plsnEnd [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/clfs/ns-clfs-_cls_lsn">CLFS_LSN</a> structure that specifies the new end of a log.  

The LSN must be between the base log sequence number (LSN) of the log and the last LSN of the log. 




### -param lpOverlapped [in, out, optional]

Reserved.  Set <i>Reserved</i> to <b>NULL</b>. 


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following  list identifies the  possible error codes:




## -remarks



If the volume sector size is greater than 512 bytes, <b>TruncateLog</b> returns ERROR_NOT_SUPPORTED.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/clfs/ns-clfs-_cls_lsn">CLFS_LSN</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-_overlapped">OVERLAPPED</a>
 

 

