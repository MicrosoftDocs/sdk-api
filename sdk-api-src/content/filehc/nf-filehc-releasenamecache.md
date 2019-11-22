---
UID: NF:filehc.ReleaseNameCache
title: ReleaseNameCache function (filehc.h)

description: Releases a name cache.
old-location: winprog\_releasenamecache.htm
tech.root: DevNotes
ms.assetid: 3abab799-4f55-40e4-9b2c-f40e92dc9af5

ms.date: 12/05/2018
ms.keywords: ReleaseNameCache, ReleaseNameCache function [Windows API], filehc/ReleaseNameCache, winprog._releasenamecache
ms.topic: function
f1_keywords: 
 - "filehc/ReleaseNameCache"
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
 - ReleaseNameCache
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ReleaseNameCache function


## -description


Releases a name cache.


## -parameters




### -param pNameCache

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/filehc/ns-filehc-name_cache_context">NAME_CACHE_CONTEXT</a> structure.


## -returns



Returns the resulting decremented reference count.




## -remarks



The caller must guarantee the thread safety of this call.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/filehc/ns-filehc-name_cache_context">NAME_CACHE_CONTEXT</a>
 

 

