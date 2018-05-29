---
UID: NF:objidl.IStream.Seek
title: IStream::Seek
author: windows-sdk-content
description: Changes the seek pointer to a new location. The new location is relative to either the beginning of the stream, the end of the stream, or the current seek pointer.
old-location: stg\istream_seek.htm
old-project: Stg
ms.assetid: ea087c6d-8854-4a81-b37b-15ab76630973
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IStream interface [Structured Storage],Seek method, IStream.Seek, IStream::Seek, Seek, Seek method [Structured Storage], Seek method [Structured Storage],IStream interface, _stg_istream_seek, objidl/IStream::Seek, stg.istream_seek
ms.prod: windows
ms.technology: windows-sdk
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
-	IStream.Seek
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IStream::Seek


## -description



			The <b>Seek</b> method changes the seek pointer to a new location.  The new location is relative to either the beginning of the stream, the end of the stream, or the current seek pointer.


## -parameters




### -param dlibMove [in]

The displacement to be added to the location indicated by the <i>dwOrigin</i> parameter. If <i>dwOrigin</i> is <b>STREAM_SEEK_SET</b>, this is interpreted as an unsigned value rather than a signed value.


### -param dwOrigin [in]

The origin for the displacement specified in <i>dlibMove</i>. The origin can be the beginning of the file (<b>STREAM_SEEK_SET</b>), the current seek pointer (<b>STREAM_SEEK_CUR</b>), or the end of the file (<b>STREAM_SEEK_END</b>). For more information about values, see the <a href="https://msdn.microsoft.com/f73a8f98-c004-40c7-b8d2-5b84d7aa2c31">STREAM_SEEK</a> enumeration.


### -param plibNewPosition [out]

A pointer to the location where this method writes the value of the new seek pointer from the beginning of the stream. 

You can set this pointer to <b>NULL</b>. In this case, this method does not provide the new seek pointer.


## -returns



This method can return one of these values.




## -remarks



<b>IStream::Seek</b> changes the seek pointer so that subsequent read and write operations can be performed at a different location in the stream object. It is an error to seek before the beginning of the stream. It is not, however, an error to seek past the end of the stream. Seeking past the end of the stream is useful for subsequent write operations, as the stream byte range will be extended to the new seek position immediately before the write is complete.

You can also use this method to obtain the current value of the seek pointer by calling this method with the <i>dwOrigin</i> parameter set to <b>STREAM_SEEK_CUR</b> and the <i>dlibMove</i> parameter set to 0 so that the seek pointer is not changed. The current seek pointer is returned in the <i>plibNewPosition</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">ISequentialStream::Read</a>



<a href="https://msdn.microsoft.com/f0323dda-6c31-4411-bf20-9650162109c0">ISequentialStream::Write</a>



<a href="https://msdn.microsoft.com/52474e37-0e14-4dcc-8e04-4442cfd26eb3">IStream - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/f73a8f98-c004-40c7-b8d2-5b84d7aa2c31">STREAM_SEEK</a>
 

 

