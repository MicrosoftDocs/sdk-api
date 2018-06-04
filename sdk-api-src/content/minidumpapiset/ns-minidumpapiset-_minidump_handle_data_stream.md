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

# _MINIDUMP_HANDLE_DATA_STREAM structure


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
<a href="https://msdn.microsoft.com/8387513a-137a-418e-8341-8066965849e6">MINIDUMP_HANDLE_DESCRIPTOR</a> or <a href="https://msdn.microsoft.com/c0678315-391c-4ce9-aa77-a88afccf79d9">MINIDUMP_HANDLE_DESCRIPTOR_2</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/8387513a-137a-418e-8341-8066965849e6">MINIDUMP_HANDLE_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/c0678315-391c-4ce9-aa77-a88afccf79d9">MINIDUMP_HANDLE_DESCRIPTOR_2</a>



<a href="https://msdn.microsoft.com/495136a0-2fed-47ca-8233-7e813b43b82f">MINIDUMP_STREAM_TYPE</a>
 

 

