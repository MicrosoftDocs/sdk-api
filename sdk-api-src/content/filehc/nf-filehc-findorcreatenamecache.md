---
UID: NF:filehc.FindOrCreateNameCache
title: FindOrCreateNameCache function
author: windows-sdk-content
description: Finds or creates a name cache.
old-location: winprog\_findorcreatenamecache.htm
tech.root: devnotes
ms.assetid: c10a501c-cc25-4586-a62a-7c7be207cbd9
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: FindOrCreateNameCache, FindOrCreateNameCache function [Windows API], filehc/FindOrCreateNameCache, winprog._findorcreatenamecache
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - FindOrCreateNameCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FindOrCreateNameCache function


## -description


Finds or creates a name cache.


## -parameters




### -param lpstrName [in]

The name of the name cache to be created. This parameter is case sensitive and must not be set to <b>NULL</b>.


### -param pfnKeyCompare [in]

A pointer to a function that is provided by a client to compare keys. This parameter cannot be <b>NULL</b>.


### -param pfnKeyHash [in]

A pointer to a function that is provided by clients to compute a hash value on keys.

<div class="alert"><b>Note</b>  The cache provides a hash function only if the user does not. However, the internally provided hash function is best only for items that appear to be regular strings.</div>
<div> </div>

### -param pfnKeyDestroy [in]

A pointer to the <a href="https://msdn.microsoft.com/daf85def-20ed-4162-b133-f730c50bf98a">CACHE_DESTROY_CALLBACK</a> function. This parameter can be <b>NULL</b>.


### -param pfnDataDestroy [in]

A pointer to the <a href="https://msdn.microsoft.com/daf85def-20ed-4162-b133-f730c50bf98a">CACHE_DESTROY_CALLBACK</a> function. This parameter can be <b>NULL</b>.


## -returns



Returns a <a href="https://msdn.microsoft.com/2d2a6066-b59a-418c-a726-0a1a39243988">NAME_CACHE_CONTEXT</a> structure that represents the name cache. 




## -remarks



Name caches are reference counted. If this function is called twice with the same name, a reference is added to an existing name cache.

The <a href="https://msdn.microsoft.com/2d2a6066-b59a-418c-a726-0a1a39243988">NAME_CACHE_CONTEXT</a> structure does not contain any fields that are useful to a client, but it must be passed back into all of the name cache functions.




## -see-also




<a href="https://msdn.microsoft.com/daf85def-20ed-4162-b133-f730c50bf98a">CACHE_DESTROY_CALLBACK</a>



<a href="https://msdn.microsoft.com/2d2a6066-b59a-418c-a726-0a1a39243988">NAME_CACHE_CONTEXT</a>
 

 

