---
UID: NF:filehc.ReleaseNameCache
title: ReleaseNameCache function
author: windows-sdk-content
description: Releases a name cache.
old-location: winprog\_releasenamecache.htm
old-project: devnotes
ms.assetid: 3abab799-4f55-40e4-9b2c-f40e92dc9af5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ReleaseNameCache, ReleaseNameCache function [Windows API], filehc/ReleaseNameCache, winprog._releasenamecache
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
 - ReleaseNameCache
product: Windows
targetos: Windows
req.lib: Fcachdll.lib
req.dll: Fcachdll.dll
req.irql: 
req.product: Internet Explorer 5
---

# ReleaseNameCache function


## -description


Releases a name cache.


## -parameters




### -param pNameCache

A pointer to a <a href="https://msdn.microsoft.com/2d2a6066-b59a-418c-a726-0a1a39243988">NAME_CACHE_CONTEXT</a> structure.


## -returns



Returns the resulting decremented reference count.




## -remarks



The caller must guarantee the thread safety of this call.




## -see-also




<a href="https://msdn.microsoft.com/2d2a6066-b59a-418c-a726-0a1a39243988">NAME_CACHE_CONTEXT</a>
 

 

