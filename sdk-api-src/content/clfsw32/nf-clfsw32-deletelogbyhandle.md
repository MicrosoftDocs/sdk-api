---
UID: NF:clfsw32.DeleteLogByHandle
title: DeleteLogByHandle function
author: windows-sdk-content
description: Marks the specified log for deletion. The log is actually deleted when all handles, marshaling areas, and read contexts to the log are closed. If the log is a physical log, its underlying containers are deleted.
old-location: fs\deletelogbyhandle.htm
old-project: Clfs
ms.assetid: 2426058f-312c-4946-ac12-52e55a3307b5
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: DeleteLogByHandle, DeleteLogByHandle function [Files], clfsw32/DeleteLogByHandle, fs.deletelogbyhandle
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
-	DeleteLogByHandle
product: Windows
targetos: Windows
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
---

# DeleteLogByHandle function


## -description


Marks the specified log for deletion. The log is actually deleted when all handles, marshaling areas, and read contexts to the log are closed.  If the log is a physical log, its underlying containers are deleted.

When a log is marked for deletion, requests to open new client log streams fail.
<div class="alert"><b>Note</b>  This function differs from <a href="https://msdn.microsoft.com/a7dd8efc-b572-4591-9e46-1cd5105d4ca2">DeleteLogFile</a>, because it takes a valid open handle to the log object instead of the log name.</div><div> </div>

## -parameters




### -param hLog [in]

A handle to an open log that is obtained by a successful call to <a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a>. The log must have been created with DELETE access or you cannot delete the log.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following list identifies the possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a>



<a href="https://msdn.microsoft.com/a7dd8efc-b572-4591-9e46-1cd5105d4ca2">DeleteLogFile</a>
 

 

