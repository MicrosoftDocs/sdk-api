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

# _MINIDUMP_THREAD_INFO_LIST structure


## -description


Contains a list of threads.


## -struct-fields




### -field SizeOfHeader

The size of the header data for the stream, in bytes. This is generally 
      <code>sizeof(MINIDUMP_THREAD_INFO_LIST)</code>.


### -field SizeOfEntry

The size of each entry following the header, in bytes. This is generally 
      <code>sizeof(MINIDUMP_THREAD_INFO)</code>.


### -field NumberOfEntries

The number of entries in the stream. These are generally 
      <a href="https://msdn.microsoft.com/855bbccb-a7c8-4744-b314-8692f785b1c0">MINIDUMP_THREAD_INFO</a> structures. The entries 
      follow the header.


## -see-also




<a href="https://msdn.microsoft.com/495136a0-2fed-47ca-8233-7e813b43b82f">MINIDUMP_STREAM_TYPE</a>



<a href="https://msdn.microsoft.com/855bbccb-a7c8-4744-b314-8692f785b1c0">MINIDUMP_THREAD_INFO</a>
 

 

