---
UID: NS:minidumpapiset._MINIDUMP_THREAD_INFO_LIST
title: "_MINIDUMP_THREAD_INFO_LIST"
author: windows-sdk-content
description: Contains a list of threads.
old-location: base\minidump_thread_info_list_str.htm
old-project: debug
ms.assetid: ee02a8fa-c81d-4b23-b8a2-6ff31cdaf3de
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PMINIDUMP_THREAD_INFO_LIST, MINIDUMP_THREAD_INFO_LIST, MINIDUMP_THREAD_INFO_LIST structure, PMINIDUMP_THREAD_INFO_LIST, PMINIDUMP_THREAD_INFO_LIST structure pointer, _MINIDUMP_THREAD_INFO_LIST, base.minidump_thread_info_list_str, minidumpapiset/MINIDUMP_THREAD_INFO_LIST, minidumpapiset/PMINIDUMP_THREAD_INFO_LIST"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: minidumpapiset.h
req.include-header: DbgHelp.h
req.redist: DbgHelp.dll 6.3 or later
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
req.typenames: MINIDUMP_THREAD_INFO_LIST, *PMINIDUMP_THREAD_INFO_LIST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_THREAD_INFO_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

