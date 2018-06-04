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

# IStream::CopyTo


## -description


The <b>CopyTo</b> method copies a specified number of bytes from the current seek pointer in the stream to the current seek pointer in another stream.


## -parameters




### -param pstm [in]

A pointer to the destination stream. The stream pointed to by <i>pstm</i> can be a new stream or a clone of the source stream.


### -param cb [in]

The number of bytes to copy from the source stream.


### -param pcbRead [out]

A pointer to the location where this method writes the actual number of bytes read from the source. You can set this pointer to <b>NULL</b>. In this case, this method does not provide the actual number of bytes read.


### -param pcbWritten [out]

A pointer to the location where this method writes the actual number of bytes written to the destination. You can set this pointer to <b>NULL</b>. In this case, this method does not provide the actual number of bytes written.


## -returns



This method can return one of these values.




## -remarks



The <b>CopyTo</b> method copies the specified bytes from one stream to another. It can also be used to copy a stream to itself. The seek pointer in each stream instance is adjusted for the number of bytes read or written. This method is equivalent to reading <i>cb</i> bytes into memory using 
<a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">ISequentialStream::Read</a> and then immediately writing them to the destination stream using 
<a href="https://msdn.microsoft.com/f0323dda-6c31-4411-bf20-9650162109c0">ISequentialStream::Write</a>, although <b>IStream::CopyTo</b> will be more efficient.

The destination stream can be a clone of the source stream created by calling the 
<a href="https://msdn.microsoft.com/677c37fb-598f-4bb0-b5d6-600e0befc722">IStream::Clone</a> method.

If <b>IStream::CopyTo</b> returns an error, you cannot assume that the seek pointers are valid for either the source or destination. Additionally, the values of <i>pcbRead</i> and <i>pcbWritten</i> are not meaningful even though they are returned.

If <b>IStream::CopyTo</b> returns successfully, the actual number of bytes read and written are the same.

To copy the remainder of the source from the current seek pointer, specify the maximum large integer value for the <i>cb</i> parameter. If the seek pointer is the beginning of the stream, this operation copies the entire stream.




## -see-also




<a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">ISequentialStream::Read</a>



<a href="https://msdn.microsoft.com/f0323dda-6c31-4411-bf20-9650162109c0">ISequentialStream::Write</a>



<a href="https://msdn.microsoft.com/52474e37-0e14-4dcc-8e04-4442cfd26eb3">IStream - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/677c37fb-598f-4bb0-b5d6-600e0befc722">IStream::Clone</a>
 

 

