---
UID: NC:filehc.CACHE_DESTROY_CALLBACK
title: CACHE_DESTROY_CALLBACK
author: windows-sdk-content
description: A function that is called whenever an entry in the name cache is destroyed.
old-location: winprog\cache_destroy_callback.htm
old-project: devnotes
ms.assetid: daf85def-20ed-4162-b133-f730c50bf98a
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: CACHE_DESTROY_CALLBACK, CACHE_DESTROY_CALLBACK callback, CACHE_DESTROY_CALLBACK callback function [Windows API], filehc/CACHE_DESTROY_CALLBACK, winprog.cache_destroy_callback
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WIN32_FIND_STREAM_DATA, *PWIN32_FIND_STREAM_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Filehc.h
api_name:
 - CACHE_DESTROY_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# CACHE_DESTROY_CALLBACK callback function


## -description


A function that is called whenever an entry in the name cache is destroyed. It provides the client with an opportunity to track any relationships between the key and data components.


## -parameters




### -param cb [in]

The size of the data or key pointed to by the <i>lpb</i> parameter, in bytes.


### -param lpb [in]

A pointer to the data or key.


## -returns



This function has no return values.




## -remarks



If the client does not associate data with the name, this function is called only for the key data.



