---
UID: NF:objidl.ISequentialStream.Read
title: ISequentialStream::Read
author: windows-driver-content
description: Reads a specified number of bytes from the stream object into memory, starting at the current seek pointer.
old-location: stg\isequentialstream_read.htm
old-project: Stg
ms.assetid: 934a90bb-5ed0-4d80-9906-352ad8586655
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: ISequentialStream interface [Structured Storage],Read method, ISequentialStream.Read, ISequentialStream::Read, Read, Read method [Structured Storage], Read method [Structured Storage],ISequentialStream interface, _stg_isequentialstream_read, objidl/ISequentialStream::Read, stg.isequentialstream_read
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ole32.dll
api_name:
-	ISequentialStream.Read
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISequentialStream::Read


## -description



			The <b>Read</b> method reads a specified number of bytes from the stream object into memory, starting at the current seek pointer.


## -parameters




### -param pv [out]

A pointer to the buffer which the stream data is read into.


### -param cb [in]

The number of bytes of data to read from the stream object.


### -param pcbRead [out]

A pointer to a <b>ULONG</b> variable that receives the actual number of bytes read from the stream object. 

<div class="alert"><b>Note</b>  The number of bytes read may be zero.</div>
<div> </div>

## -returns



This method can return one of these values.




## -remarks



This method reads bytes from this stream object into memory. The stream object must be opened in <b>STGM_READ</b> mode. This method adjusts the seek pointer by the actual number of bytes read.

The number of bytes actually read is also returned in the <i>pcbRead</i> parameter.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The actual number of bytes read can be less than the number of bytes requested if an error occurs or if the end of the stream is reached during the read operation.  The number of bytes returned should always  be compared to the number of bytes requested.  If the number of bytes returned is less than the number of bytes requested, it usually means the <b>Read</b> method attempted to read  past the end of the stream.

The application should handle both a returned error  and <b>S_OK</b> return values on end-of-stream read operations.




## -see-also




<a href="https://msdn.microsoft.com/f0323dda-6c31-4411-bf20-9650162109c0">ISequentialStream::Write</a>



<a href="https://msdn.microsoft.com/f7bd1f26-e9a3-415d-8cd3-dc34f7ad8feb">IStorage::OpenStream</a>



<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>



<a href="https://msdn.microsoft.com/52474e37-0e14-4dcc-8e04-4442cfd26eb3">IStream - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/f55c376b-f150-406a-b960-f096c2deeff1">STGMOVE</a>
 

 

