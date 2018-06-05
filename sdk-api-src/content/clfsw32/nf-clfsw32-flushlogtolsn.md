---
UID: NF:clfsw32.FlushLogToLsn
title: FlushLogToLsn function
author: windows-sdk-content
description: Forces all records appended to this marshaling area up to the record with the specified log sequence number (LSN) to be flushed to the disk. More records than specified may be flushed during this operation.
old-location: fs\flushlogtolsn.htm
old-project: Clfs
ms.assetid: d2a30ce1-e9c7-4dcf-b5fb-4355c9134461
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: FlushLogToLsn, FlushLogToLsn function [Files], clfsw32/FlushLogToLsn, fs.flushlogtolsn
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: LOG_MANAGEMENT_CALLBACKS, *PLOG_MANAGEMENT_CALLBACKS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Clfsw32.dll
api_name:
-	FlushLogToLsn
product: Windows
targetos: Windows
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
---

# FlushLogToLsn function


## -description


Forces all records appended to this marshaling area up to the record with the specified log sequence number (LSN) to be flushed to the disk.  More records than specified may be flushed during this operation.


## -parameters




### -param pvMarshalContext [in]

A pointer to the  marshaling context that is allocated by using the <a href="https://msdn.microsoft.com/750c0615-bfac-402b-a590-6c9d800cf2d8">CreateLogMarshallingArea</a> function.


### -param plsnFlush [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff541824">CLFS_LSN</a> structure that specifies the LSN that is used to determine which records to flush.   

Specify CLFS_LSN_NULL to flush all records in the marshaling area. 


### -param OPTIONAL

TBD




#### - pOverlapped [in, out, optional]

A pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure that  is required for asynchronous operation. 

This parameter can be <b>NULL</b>  except for an asynchronous operation.


#### - plsnLastFlushed [out, optional]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff541824">CLFS_LSN</a> structure. 

The LSN returned is greater than the LSN of any record flushed.  If the function  succeeds, the value of the LSN is never less than <i>plsnFlush</i>.  This value  is meaningful only  when  the function succeeds.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following list identifies the   possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541824">CLFS_LSN</a>



<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>
 

 

