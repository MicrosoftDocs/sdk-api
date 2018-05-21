---
UID: NF:clfsw32.DeleteLogMarshallingArea
title: DeleteLogMarshallingArea function
author: windows-driver-content
description: Deletes a marshaling area that is created by a successful call to CreateLogMarshallingArea.
old-location: fs\deletelogmarshallingarea.htm
old-project: Clfs
ms.assetid: d58bd64f-fa76-4ab3-9660-e31e9029171c
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: DeleteLogMarshallingArea, DeleteLogMarshallingArea function [Files], clfsw32/DeleteLogMarshallingArea, fs.deletelogmarshalingarea, fs.deletelogmarshallingarea
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
req.typenames: LOG_MANAGEMENT_CALLBACKS, *PLOG_MANAGEMENT_CALLBACKS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Clfsw32.dll
api_name:
-	DeleteLogMarshallingArea
product: Windows
targetos: Windows
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
---

# DeleteLogMarshallingArea function


## -description


Deletes a marshaling area that is created by a successful call to <a href="https://msdn.microsoft.com/750c0615-bfac-402b-a590-6c9d800cf2d8">CreateLogMarshallingArea</a>.

When you delete a marshaling area it does the following:<ul>
<li>Flushes the log to free pending log I/O blocks</li>
<li>Deallocates all log I/O blocks and invalidates all read contexts</li>
</ul>   The memory allocated by Common Log File System (CLFS)  to create the marshaling context is reclaimed when all read contexts are terminated.
<div class="alert"><b>Note</b>  Clients should not delete a marshaling area if there are pending  operations on the marshaling area.</div><div> </div>

## -parameters




### -param pvMarshal [in]

A pointer to the opaque marshaling context allocated by using the <a href="https://msdn.microsoft.com/750c0615-bfac-402b-a590-6c9d800cf2d8">CreateLogMarshallingArea</a> function.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following list identifies the possible  error codes:




## -see-also




<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/750c0615-bfac-402b-a590-6c9d800cf2d8">CreateLogMarshallingArea</a>
 

 

