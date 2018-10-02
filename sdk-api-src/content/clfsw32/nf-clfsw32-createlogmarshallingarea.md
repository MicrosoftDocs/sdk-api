---
UID: NF:clfsw32.CreateLogMarshallingArea
title: CreateLogMarshallingArea function
author: windows-sdk-content
description: Creates a marshaling area for a log, and when successful it returns a marshaling context. Before creating a marshaling area, the log must have at least one container.
old-location: fs\createlogmarshallingarea.htm
tech.root: Clfs
ms.assetid: 750c0615-bfac-402b-a590-6c9d800cf2d8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateLogMarshallingArea, CreateLogMarshallingArea function [Files], clfsw32/CreateLogMarshallingArea, fs.createlogmarshalingarea, fs.createlogmarshallingarea
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
 - CreateLogMarshallingArea
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateLogMarshallingArea function


## -description


Creates a marshaling area for a log, and when successful it returns  a  marshaling context. Before creating a marshaling area, the log must have at least one container.



The marshaling context is used to append records to or read records from a log.  Because records are always stored in log blocks, they must pass through the marshaling context.

Log records are written by calling <a href="https://msdn.microsoft.com/2036fc26-d040-4738-b66e-d5d3d0dbe385">ReserveAndAppendLog</a>.


## -parameters




### -param hLog [in]

A handle to the log that is obtained from <a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a>.  

The log handle  can  refer to a dedicated or multiplexed log.


### -param pfnAllocBuffer [in, optional]

The callback function that allocates memory for log blocks.  

If this parameter is <b>NULL</b>, the Common Log File System (CLFS) provides a default block allocation function.  This parameter cannot be <b>NULL</b> if a block-freeing callback is specified by using the <i>pfnFreeBuffer</i>  parameter.

The following example identifies the  syntax of the block allocation callback function:

<code>typedef PVOID (* CLFS_BLOCK_ALLOCATION) (ULONG cbBufferSize, PVOID pvUserContext);</code>


### -param pfnFreeBuffer [in, optional]

The callback function that   frees log blocks allocated by <i>pfnAllocBuffer</i>.  

If this parameter is <b>NULL</b>, CLFS provides a default block deallocation function.  This parameter cannot be <b>NULL</b> if a block allocation callback is specified by using the <i>pfnAllocBuffer</i> parameter.

The following example identifies the syntax of the  block-freeing callback function:

<code>typedef void (* CLFS_BLOCK_DEALLOCATION) (PVOID pvBuffer, PVOID pvUserContext);</code>

The <i>buffer</i> parameter of "ClfsBlockDeallocProc" must point to a block that is allocated by using the callback pointed to by <i>pfnAllocBuffer</i>.


### -param pvBlockAllocContext [in, optional]

A pointer to a  buffer that is passed back as a user context to the block allocation and deallocation routines, if a buffer is specified.  

If <i>pfnAllocBuffer</i> is <b>NULL</b>, this parameter is ignored.


### -param cbMarshallingBuffer [in]

The size, in bytes, of the individual log I/O blocks that will be used by the new marshaling area.  This must be a multiple of the sector size on the stable storage medium.   The sector size is the value returned in the <i>lpBytesPerSector</i> parameter of the <a href="https://msdn.microsoft.com/4fe14c49-3fd6-48b7-92de-a0c867b2e042">GetDiskFreeSpace</a> function.

Records cannot be appended or read if they are longer than this value.


### -param cMaxWriteBuffers [in]

The maximum number of blocks that can be allocated at any time for   write operations.  

This value can affect the frequency of data flushes. If you do not need to specify a limit to control the frequency of the  data flush cycle, specify  INFINITE. 


### -param cMaxReadBuffers [in]

The maximum number of blocks that can be allocated at any time for read operations.  

Read contexts use at least one read block.  


### -param ppvMarshal [out]

A pointer to the  marshaling context  that CLFS  allocates when <b>CreateLogMarshallingArea</b> completes successfully.  

This context must be used with all read, append, write, and flush operations to log marshaling areas.  All operations that access marshaling areas by using a marshaling context are thread-safe. This parameter is <b>NULL</b> if the operation is not successful.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following  list identifies the  possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a>



<a href="https://msdn.microsoft.com/d58bd64f-fa76-4ab3-9660-e31e9029171c">DeleteLogMarshallingArea</a>
 

 

