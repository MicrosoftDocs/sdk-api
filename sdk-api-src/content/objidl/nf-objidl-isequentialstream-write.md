---
UID: NF:objidl.ISequentialStream.Write
title: ISequentialStream::Write (objidl.h)
author: windows-sdk-content
description: Writes a specified number of bytes into the stream object starting at the current seek pointer.
old-location: stg\isequentialstream_write.htm
tech.root: Stg
ms.assetid: f0323dda-6c31-4411-bf20-9650162109c0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISequentialStream interface [Structured Storage],Write method, ISequentialStream.Write, ISequentialStream::Write, Write, Write method [Structured Storage], Write method [Structured Storage],ISequentialStream interface, _stg_isequentialstream_write, objidl/ISequentialStream::Write, stg.isequentialstream_write
ms.topic: method
f1_keywords: 
 - "objidl/ISequentialStream.Write"
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
 - ISequentialStream.Write
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISequentialStream::Write


## -description


The <b>Write</b> method writes a specified number of bytes into the stream object starting at the current seek pointer.


## -parameters




### -param pv [in]

A pointer to the buffer that contains the data that is to be written to the stream. A valid pointer must be provided for this parameter even when <i>cb</i> is zero.


### -param cb [in]

The number of bytes of data to attempt to write into the stream. This value can be zero.


### -param pcbWritten [out]

A pointer to a <b>ULONG</b> variable where this method writes the actual number of bytes written to the stream object. The caller can set this pointer to <b>NULL</b>, in which case this method does not provide the actual number of bytes written.


## -returns



This method can return one of these values.




## -remarks



<b>ISequentialStream::Write</b> writes the specified data to a stream object. The seek pointer is adjusted for the number of bytes actually written. The number of bytes actually written is returned in the <i>pcbWritten</i> parameter. If the byte count is zero bytes, the write operation has no effect.

If the seek pointer is currently past the end of the stream and the byte count is nonzero, this method increases the size of the stream to the seek pointer and writes the specified bytes starting at the seek pointer. The fill bytes written to the stream are not initialized to any particular value. This is the same as the end-of-file behavior in the MS-DOS FAT file system.

With a zero byte count and a seek pointer past the end of the stream, this method does not create the fill bytes to increase the stream to the seek pointer. In this case, you must call the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-setsize">IStream::SetSize</a> method to increase the size of the stream and write the fill bytes.

The <i>pcbWritten</i> parameter can have a value even if an error occurs.

In the COM-provided implementation, stream objects are not sparse. Any fill bytes are eventually allocated on the disk and assigned to the stream.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">ISequentialStream::Read</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-openstream">IStorage::OpenStream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>



<a href="https://docs.microsoft.com/windows/desktop/Stg/istream-compound-file-implementation">IStream - Compound File Implementation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ne-wtypes-stgmove">STGMOVE</a>
 

 

