---
UID: NF:clfsw32.TerminateReadLog
title: TerminateReadLog function
author: windows-sdk-content
description: Terminates a read context. This function frees system-allocated resources associated with the specified read context. Do not attempt to read log records after calling this function; you will receive indeterminate results.
old-location: fs\terminatereadlog.htm
tech.root: Clfs
ms.assetid: fb0a4c4e-cdb7-4c42-9102-bc76b8b70193
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: TerminateReadLog, TerminateReadLog function [Files], clfsw32/TerminateReadLog, fs.terminatereadlog
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
 - TerminateReadLog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TerminateReadLog function


## -description


Terminates a read context. This function frees system-allocated resources associated with the specified read context. Do not attempt to read log records after calling this function; you will receive indeterminate results.




## -parameters




### -param pvCursorContext [in]

A pointer to a  read context that is returned by <a href="https://msdn.microsoft.com/1c56c47b-d898-4c70-ba70-8978057c66b9">ReadLogRecord</a> or <a href="https://msdn.microsoft.com/ab59d2fe-d951-42f3-b270-844eaeb6ff90">ReadLogRestartArea</a>.  


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following  list identifies the possible error codes:




## -remarks



It is important to deallocate unused read contexts.  Failure to call this function causes resource leaks.




## -see-also




<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/1c56c47b-d898-4c70-ba70-8978057c66b9">ReadLogRecord</a>



<a href="https://msdn.microsoft.com/ab59d2fe-d951-42f3-b270-844eaeb6ff90">ReadLogRestartArea</a>
 

 

