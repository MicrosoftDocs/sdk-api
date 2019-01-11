---
UID: NF:filehc.CacheRichCreateFile
title: CacheRichCreateFile function
author: windows-sdk-content
description: Creates a file in the cache or finds an existing file and allows properties to be added to it in the cache.
old-location: winprog\_cacherichcreatefile.htm
tech.root: DevNotes
ms.assetid: 89b0adcd-0084-4538-b162-661ddae53dc8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CacheRichCreateFile, CacheRichCreateFile function [Windows API], filehc/CacheRichCreateFile, winprog._cacherichcreatefile
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
req.lib: Fcachdll.lib
req.dll: Fcachdll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fcachdll.dll
api_name:
 - CacheRichCreateFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CacheRichCreateFile function


## -description


Creates a file in the cache or finds an existing file and allows properties to be added to it in the cache.


## -parameters




### -param lpstrName [in]

A pointer to the name of the file to be created in the cache.


### -param pfnCallBack [in]

A pointer to the <a href="https://msdn.microsoft.com/86e0d47e-469b-4c1d-9e39-f4f6d9e58ba0">FCACHE_RICHCREATE_CALLBACK</a> function that was used to create the file.


### -param lpv [in]

 If the file is not in the cache, the call calls <i>pfnCallBack</i> with <i>lpv</i> to do the actual work of calling <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>.


### -param fAsyncContext [in]

Specifies whether the context can be used for asynchronous I/O. If <b>TRUE</b>, the <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> returned is asynchronous.


## -returns



Returns the address of the <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure that was obtained.




## -see-also




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/86e0d47e-469b-4c1d-9e39-f4f6d9e58ba0">FCACHE_RICHCREATE_CALLBACK</a>



<a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a>
 

 

