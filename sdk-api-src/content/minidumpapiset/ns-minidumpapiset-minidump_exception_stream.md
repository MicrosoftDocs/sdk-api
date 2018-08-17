---
UID: NS:minidumpapiset.MINIDUMP_EXCEPTION_STREAM
title: MINIDUMP_EXCEPTION_STREAM
author: windows-sdk-content
description: Represents an exception information stream.
old-location: base\minidump_exception_stream_str.htm
old-project: debug
ms.assetid: 2de717dc-a9ac-4b81-9fab-992f22da9a0d
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: "*PMINIDUMP_EXCEPTION_STREAM, MINIDUMP_EXCEPTION_STREAM, MINIDUMP_EXCEPTION_STREAM structure, PMINIDUMP_EXCEPTION_STREAM, PMINIDUMP_EXCEPTION_STREAM structure pointer, _win32_minidump_exception_stream_str, base.minidump_exception_stream_str, minidumpapiset/MINIDUMP_EXCEPTION_STREAM, minidumpapiset/PMINIDUMP_EXCEPTION_STREAM"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: minidumpapiset.h
req.include-header: DbgHelp.h
req.redist: DbgHelp.dll 5.1 or later
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
req.typenames: MINIDUMP_EXCEPTION_STREAM, *PMINIDUMP_EXCEPTION_STREAM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_EXCEPTION_STREAM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MINIDUMP_EXCEPTION_STREAM structure


## -description


Represents an exception information stream.


## -struct-fields




### -field ThreadId

The identifier of the thread that caused the exception.


### -field __alignment

A variable for alignment.


### -field ExceptionRecord

A 
<a href="https://msdn.microsoft.com/edbb87a7-1b99-46bd-8797-c806861ec73a">MINIDUMP_EXCEPTION</a> structure.


### -field ThreadContext

A 
<a href="https://msdn.microsoft.com/aef17239-9b56-4d49-8347-610270f8612b">MINIDUMP_LOCATION_DESCRIPTOR</a> structure.


## -remarks



In this context, a data stream is a set of data in a minidump file.




## -see-also




<a href="https://msdn.microsoft.com/edbb87a7-1b99-46bd-8797-c806861ec73a">MINIDUMP_EXCEPTION</a>



<a href="https://msdn.microsoft.com/aef17239-9b56-4d49-8347-610270f8612b">MINIDUMP_LOCATION_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/495136a0-2fed-47ca-8233-7e813b43b82f">MINIDUMP_STREAM_TYPE</a>
 

 

