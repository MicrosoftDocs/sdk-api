---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# AuxUlibSetSystemFileCacheSize function


## -description


Sets the current file system cache size.

As of Windows Server 2003 with Service Pack 1 (SP1), this function has been superseded by the <a href="https://msdn.microsoft.com/bb0a65d6-d04a-4805-80d5-61fc53eb2726">SetSystemFileCacheSize</a> function.


## -parameters




### -param MinimumFileCacheSize

TBD


### -param MaximumFileCacheSize

TBD


### -param Flags

TBD




#### - dwFlags [in]

This parameter is reserved for future use and must be zero.


#### - dwMaximumFileCacheSize [in]

The maximum cache size, in bytes. To flush the cache, use (<b>DWORD</b>)–1.


#### - dwMinimumFileCacheSize [in]

The minimum cache size, in bytes. To flush the cache, use (<b>DWORD</b>)–1.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



You must call the <a href="https://msdn.microsoft.com/2e46e323-669c-4fcd-b3e0-d1e4ec700c64">AuxUlibInitialize</a> function before calling this function.

The caller must have enabled the SE_INCREASE_QUOTA_NAME privilege in the active token.

The object library that implements this API can be downloaded from <a href="Http://go.microsoft.com/fwlink/p/?linkid=85311">here</a>.




## -see-also




<a href="https://msdn.microsoft.com/2e46e323-669c-4fcd-b3e0-d1e4ec700c64">AuxUlibInitialize</a>
 

 

