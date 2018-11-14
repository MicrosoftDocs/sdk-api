---
UID: NF:clfsw32.TruncateLog
title: TruncateLog function
author: windows-sdk-content
description: Truncates the log. The function sets the end of the log to the specified value.
old-location: fs\truncatelog.htm
tech.root: Clfs
ms.assetid: 76ef1a01-ba5c-4419-ac2f-4ba53dcc5bc4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: TruncateLog, TruncateLog function [Files], clfsw32/TruncateLog, fs.truncatelog
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - TruncateLog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- TruncateLog
: 
---

# TruncateLog function


## -description


Truncates the log. The function sets the end of the log to the specified value.


## -parameters




### -param pvMarshal [in]

A pointer to the opaque marshaling context that is allocated by calling the <a href="https://msdn.microsoft.com/750c0615-bfac-402b-a590-6c9d800cf2d8">CreateLogMarshallingArea</a> function.


### -param plsnEnd [in]

A pointer to a <a href="https://msdn.microsoft.com/f388feec-e1dc-4ae9-aa33-8f2fdc4dbc9a">CLFS_LSN</a> structure that specifies the new end of a log.  

The LSN must be between the base log sequence number (LSN) of the log and the last LSN of the log. 




### -param lpOverlapped [in, out, optional]

Reserved.  Set <i>Reserved</i> to <b>NULL</b>. 


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following  list identifies the  possible error codes:




## -remarks



If the volume sector size is greater than 512 bytes, <b>TruncateLog</b> returns ERROR_NOT_SUPPORTED.




## -see-also




<a href="https://msdn.microsoft.com/f388feec-e1dc-4ae9-aa33-8f2fdc4dbc9a">CLFS_LSN</a>



<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>
 

 

