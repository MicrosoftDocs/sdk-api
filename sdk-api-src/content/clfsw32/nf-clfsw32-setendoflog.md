---
UID: NF:clfsw32.SetEndOfLog
title: SetEndOfLog function (clfsw32.h)
author: windows-sdk-content
description: This function has been deprecated. Use TruncateLog instead.
old-location: fs\setendoflog.htm
tech.root: Clfs
ms.assetid: ef4f123f-3e1a-4082-93c7-f23783b1d45e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetEndOfLog, SetEndOfLog function [Files], clfsw32/SetEndOfLog, fs.setendoflog
ms.topic: function
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
 - SetEndOfLog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetEndOfLog function


## -description


This function has been deprecated.  Use <a href="https://msdn.microsoft.com/76ef1a01-ba5c-4419-ac2f-4ba53dcc5bc4">TruncateLog</a> instead. 


## -parameters




### -param hLog [in]

 A handle to the log that is obtained from <a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a>.  

The log handle must refer to a dedicated log.


### -param plsnEnd [in]

A pointer to a <a href="https://msdn.microsoft.com/f388feec-e1dc-4ae9-aa33-8f2fdc4dbc9a">CLFS_LSN</a> structure that specifies the new end of a log.  

The LSN must be between the base log sequence number (LSN) of the log and the last LSN of the log. 




### -param lpOverlapped [in, out, optional]

Reserved.  Set <i>lpOverlapped</i> to <b>NULL</b>. 


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following  list identifies the  possible error codes:




## -remarks



The <b>SetEndOfLog</b> function  truncates the log by setting the end of the log to the specified value.   This operation only works on dedicated logs.

<b>SetEndOfLog</b> can only be used to truncate a log.




## -see-also




<a href="https://msdn.microsoft.com/f388feec-e1dc-4ae9-aa33-8f2fdc4dbc9a">CLFS_LSN</a>



<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>
 

 

