---
UID: NF:filehc.CacheCreateFile
title: CacheCreateFile function (filehc.h)
description: Creates a file in the cache or finds an existing file.
helpviewer_keywords: ["CacheCreateFile","CacheCreateFile function [Windows API]","filehc/CacheCreateFile","winprog._cachecreatefile"]
old-location: winprog\_cachecreatefile.htm
tech.root: winprog
ms.assetid: 089160c7-eb30-4b39-b982-75356e7cdb24
ms.date: 12/05/2018
ms.keywords: CacheCreateFile, CacheCreateFile function [Windows API], filehc/CacheCreateFile, winprog._cachecreatefile
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CacheCreateFile
 - filehc/CacheCreateFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fcachdll.dll
api_name:
 - CacheCreateFile
---

# CacheCreateFile function


## -description

Creates a file in the cache or finds an existing file.

## -parameters

### -param lpstrName [in]

A pointer to the name of the file to be created in the cache.

### -param pfnCallBack [in]

A pointer to the <a href="/previous-versions/bb432261(v=vs.85)">FCACHE_CREATE_CALLBACK</a> function that was used to create the file.

### -param lpv [in]

 If the file is not in the cache, the call calls <i>pfnCallBack</i> with <i>lpv</i> to do the actual work of calling <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>.

### -param fAsyncContext [in]

Specifies whether the context can be used for asynchronous I/O. If <b>TRUE</b>, the <a href="/previous-versions/exchange-server/exchange-10/ms528326(v=exchg.10)">FIO_CONTEXT</a> returned is asynchronous.

## -returns

Returns a pointer to the <a href="/previous-versions/exchange-server/exchange-10/ms528326(v=exchg.10)">FIO_CONTEXT</a> structure that is associated with the file that was created or found.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/previous-versions/bb432261(v=vs.85)">FCACHE_CREATE_CALLBACK</a>



<a href="/previous-versions/exchange-server/exchange-10/ms528326(v=exchg.10)">FIO_CONTEXT</a>