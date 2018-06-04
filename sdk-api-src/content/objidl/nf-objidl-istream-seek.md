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
 

 

