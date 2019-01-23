---
UID: NS:minidumpapiset._MINIDUMP_HANDLE_DATA_STREAM
title: MINIDUMP_HANDLE_DATA_STREAM
author: windows-sdk-content
description: Represents the header for a handle data stream.
old-location: base\minidump_handle_data_stream_str.htm
tech.root: debug
ms.assetid: 5674df6b-77e0-4bca-8349-8217388902ed
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PMINIDUMP_HANDLE_DATA_STREAM, MINIDUMP_HANDLE_DATA_STREAM, MINIDUMP_HANDLE_DATA_STREAM structure, PMINIDUMP_HANDLE_DATA_STREAM, PMINIDUMP_HANDLE_DATA_STREAM structure pointer, _MINIDUMP_HANDLE_DATA_STREAM, _win32_minidump_handle_data_stream_str, base.minidump_handle_data_stream_str, minidumpapiset/MINIDUMP_HANDLE_DATA_STREAM, minidumpapiset/PMINIDUMP_HANDLE_DATA_STREAM"
ms.topic: struct
req.header: minidumpapiset.h
req.include-header: DbgHelp.h
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
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_HANDLE_DATA_STREAM
product: Windows
targetos: Windows
req.typenames: MINIDUMP_HANDLE_DATA_STREAM, *PMINIDUMP_HANDLE_DATA_STREAM
req.redist: DbgHelp.dll 5.1 or later
---

# MINIDUMP_HANDLE_DATA_STREAM structure


## -description


Represents the header for a handle data stream.


## -struct-fields




### -field SizeOfHeader

The size of the header information for the stream, in bytes. This value is <code>sizeof(MINIDUMP_HANDLE_DATA_STREAM)</code>.


### -field SizeOfDescriptor

The size of a descriptor in the stream, in bytes. This value is <code>sizeof(MINIDUMP_HANDLE_DESCRIPTOR)</code> or <code>sizeof(MINIDUMP_HANDLE_DESCRIPTOR_2)</code>.


### -field NumberOfDescriptors

The number of descriptors in the stream.


### -field Reserved

Reserved for future use; must be zero.


## -remarks



In this context, a data stream is a set of data in a minidump file. This header structure is followed by <b>NumberOfDescriptors</b>
<a href="https://msdn.microsoft.com/en-us/library/ms680374(v=VS.85).aspx">MINIDUMP_HANDLE_DESCRIPTOR</a> or <a href="https://msdn.microsoft.com/en-us/library/ms680373(v=VS.85).aspx">MINIDUMP_HANDLE_DESCRIPTOR_2</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680374(v=VS.85).aspx">MINIDUMP_HANDLE_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680373(v=VS.85).aspx">MINIDUMP_HANDLE_DESCRIPTOR_2</a>



<a href="https://msdn.microsoft.com/495136a0-2fed-47ca-8233-7e813b43b82f">MINIDUMP_STREAM_TYPE</a>
 

 

