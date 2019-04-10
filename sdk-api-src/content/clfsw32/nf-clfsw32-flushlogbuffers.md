---
UID: NF:clfsw32.FlushLogBuffers
title: FlushLogBuffers function (clfsw32.h)
author: windows-sdk-content
description: Forces all records appended to this marshaling area to be flushed to disk.
old-location: fs\flushlogbuffers.htm
tech.root: Clfs
ms.assetid: b5c52472-6c08-44f6-843f-5206611e40b4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FlushLogBuffers, FlushLogBuffers function [Files], clfsw32/FlushLogBuffers, fs.flushlogbuffers
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
 - FlushLogBuffers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FlushLogBuffers function


## -description


Forces all records appended to this marshaling area to be flushed to  disk.  This service is a special case of <a href="https://msdn.microsoft.com/d2a30ce1-e9c7-4dcf-b5fb-4355c9134461">FlushLogToLsn</a> with the target log sequence number (LSN) set to <b>CLFS_LSN_NULL</b>.


## -parameters




### -param pvMarshal [in]

A pointer to the  marshaling context that is allocated by using the <a href="https://msdn.microsoft.com/750c0615-bfac-402b-a590-6c9d800cf2d8">CreateLogMarshallingArea</a> function.


### -param pOverlapped [in, out, optional]

A pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure that  is required for asynchronous operation. 

This parameter can be <b>NULL</b> if asynchronous operation is not used.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following list identifies the  possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/d2a30ce1-e9c7-4dcf-b5fb-4355c9134461">FlushLogToLsn</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>
 

 

