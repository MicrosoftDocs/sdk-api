---
UID: NF:clfsw32.TerminateLogArchive
title: TerminateLogArchive function
author: windows-sdk-content
description: Deallocates system resources that are allocated originally for a log archive context by PrepareLogArchive.
old-location: fs\terminatelogarchive.htm
old-project: Clfs
ms.assetid: 885356e1-f7c4-4f3f-98c3-fb9b1d339e22
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: TerminateLogArchive, TerminateLogArchive function [Files], clfsw32/TerminateLogArchive, fs.terminatelogarchive
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
-	TerminateLogArchive
product: Windows
targetos: Windows
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
---

# TerminateLogArchive function


## -description


Deallocates  system resources that are  allocated originally for  a log archive context by   <a href="https://msdn.microsoft.com/dfdad56a-7485-4c23-852e-819980ecd5e9">PrepareLogArchive</a>.


## -parameters




### -param pvArchiveContext [in]

The archive context that is obtained from <a href="https://msdn.microsoft.com/dfdad56a-7485-4c23-852e-819980ecd5e9">PrepareLogArchive</a>.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following  error code is possible:




## -remarks




        Failure to call this function after archiving  completes  results in a resource leak.




## -see-also




<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/dfdad56a-7485-4c23-852e-819980ecd5e9">PrepareLogArchive</a>
 

 

