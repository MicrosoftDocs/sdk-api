---
UID: NC:filehc.FCACHE_CREATE_CALLBACK
title: FCACHE_CREATE_CALLBACK (filehc.h)
author: windows-sdk-content
description: A callback function that is used to create items in the cache.
old-location: winprog\fcache_create_callback.htm
tech.root: DevNotes
ms.assetid: e6e20409-3cbc-4d04-b861-ebed7d15af6a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FCACHE_CREATE_CALLBACK, FCACHE_CREATE_CALLBACK callback, FCACHE_CREATE_CALLBACK callback function [Windows API], filehc/FCACHE_CREATE_CALLBACK, winprog.fcache_create_callback
ms.topic: callback
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Filehc.h
api_name:
 - FCACHE_CREATE_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FCACHE_CREATE_CALLBACK callback function


## -description


A callback function that is used to create items in the cache. It is called by the <a href="https://msdn.microsoft.com/089160c7-eb30-4b39-b982-75356e7cdb24">CacheCreateFile</a> function.


## -parameters




### -param lpstrName [in]

The name of the file.


### -param lpvData [in]

User-provided data to <a href="https://msdn.microsoft.com/089160c7-eb30-4b39-b982-75356e7cdb24">CacheCreateFile</a>.


### -param *cbFileSize [out]

The size of the file.


### -param *cbFileSizeHigh [out]

The location to return the high <b>DWORD</b> of the file size.


## -returns



Returns a handle to the file created in the cache.




## -see-also




<a href="https://msdn.microsoft.com/089160c7-eb30-4b39-b982-75356e7cdb24">CacheCreateFile</a>
 

 

