---
UID: NF:filehc.CacheCreateFile
title: CacheCreateFile function
author: windows-sdk-content
description: Creates a file in the cache or finds an existing file.
old-location: winprog\_cachecreatefile.htm
old-project: DevNotes
ms.assetid: 089160c7-eb30-4b39-b982-75356e7cdb24
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CacheCreateFile, CacheCreateFile function [Windows API], filehc/CacheCreateFile, winprog._cachecreatefile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: filehc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: WIN32_FIND_STREAM_DATA, *PWIN32_FIND_STREAM_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fcachdll.dll
api_name:
 - CacheCreateFile
product: Windows
targetos: Windows
req.lib: Fcachdll.lib
req.dll: Fcachdll.dll
req.irql: 
req.product: Internet Explorer 5
---

# CacheCreateFile function


## -description


Creates a file in the cache or finds an existing file.


## -parameters




### -param lpstrName [in]

A pointer to the name of the file to be created in the cache.


### -param pfnCallBack [in]

A pointer to the <a href="https://msdn.microsoft.com/e6e20409-3cbc-4d04-b861-ebed7d15af6a">FCACHE_CREATE_CALLBACK</a> function that was used to create the file.


### -param lpv [in]

 If the file is not in the cache, the call calls <i>pfnCallBack</i> with <i>lpv</i> to do the actual work of calling <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>.


### -param fAsyncContext [in]

Specifies whether the context can be used for asynchronous I/O. If <b>TRUE</b>, the <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> returned is asynchronous. 


## -returns



Returns a pointer to the <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure that is associated with the file that was created or found.




## -see-also




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/e6e20409-3cbc-4d04-b861-ebed7d15af6a">FCACHE_CREATE_CALLBACK</a>



<a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a>
 

 

