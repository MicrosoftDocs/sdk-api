---
UID: NF:objidl.IStream.CopyTo
title: IStream::CopyTo
author: windows-sdk-content
description: Copies a specified number of bytes from the current seek pointer in the stream to the current seek pointer in another stream.
old-location: stg\istream_copyto.htm
tech.root: stg
ms.assetid: 5bcd7da6-8bd5-4ab7-952f-f0a12e87f2d4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CopyTo, CopyTo method [Structured Storage], CopyTo method [Structured Storage],IStream interface, IStream interface [Structured Storage],CopyTo method, IStream.CopyTo, IStream::CopyTo, _stg_istream_copyto, objidl/IStream::CopyTo, stg.istream_copyto
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IStream.CopyTo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

