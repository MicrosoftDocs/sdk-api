---
UID: NF:filehc.CacheRichCreateFile
title: CacheRichCreateFile function (filehc.h)
description: Creates a file in the cache or finds an existing file and allows properties to be added to it in the cache.helpviewer_keywords: ["CacheRichCreateFile","CacheRichCreateFile function [Windows API]","filehc/CacheRichCreateFile","winprog._cacherichcreatefile"]
old-location: winprog\_cacherichcreatefile.htm
tech.root: DevNotes
ms.assetid: 89b0adcd-0084-4538-b162-661ddae53dc8
ms.date: 12/05/2018
ms.keywords: CacheRichCreateFile, CacheRichCreateFile function [Windows API], filehc/CacheRichCreateFile, winprog._cacherichcreatefile
f1_keywords:
- filehc/CacheRichCreateFile
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CacheRichCreateFile function


## -description


Creates a file in the cache or finds an existing file and allows properties to be added to it in the cache.


## -parameters




### -param lpstrName [in]

A pointer to the name of the file to be created in the cache.


### -param pfnCallBack [in]

A pointer to the <a href="https://docs.microsoft.com/previous-versions/bb432263(v=vs.85)">FCACHE_RICHCREATE_CALLBACK</a> function that was used to create the file.


### -param lpv [in]

 If the file is not in the cache, the call calls <i>pfnCallBack</i> with <i>lpv</i> to do the actual work of calling <a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>.


### -param fAsyncContext [in]

Specifies whether the context can be used for asynchronous I/O. If <b>TRUE</b>, the <a href="https://msdn.microsoft.com/library/ms528326.aspx">FIO_CONTEXT</a> returned is asynchronous.


## -returns



Returns the address of the <a href="https://msdn.microsoft.com/library/ms528326.aspx">FIO_CONTEXT</a> structure that was obtained.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="https://docs.microsoft.com/previous-versions/bb432263(v=vs.85)">FCACHE_RICHCREATE_CALLBACK</a>



<a href="https://msdn.microsoft.com/library/ms528326.aspx">FIO_CONTEXT</a>
 

 

