---
UID: NF:vfw.IAVIStream.Read
title: IAVIStream::Read
author: windows-sdk-content
description: The Read method reads data from a stream and copies it to an application-defined buffer. If no buffer is supplied, it determines the buffer size needed to retrieve the next buffer of data. Called when an application uses the AVIStreamRead function.
old-location: multimedia\iavistream_read.htm
tech.root: Multimedia
ms.assetid: 95835ba2-5085-467f-ae2c-27dd4d2ea68c
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IAVIStream interface [Windows Multimedia],Read method, IAVIStream.Read, IAVIStream::Read, Read, Read method [Windows Multimedia], Read method [Windows Multimedia],IAVIStream interface, _win32_IAVIStream_Read, multimedia.iavistream_read, vfw/IAVIStream::Read
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vfw32.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vfw32.lib
 - Vfw32.dll
api_name:
 - IAVIStream.Read
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAVIStream::Read


## -description



The <b>Read</b> method reads data from a stream and copies it to an application-defined buffer. If no buffer is supplied, it determines the buffer size needed to retrieve the next buffer of data. Called when an application uses the <a href="https://msdn.microsoft.com/9490d46f-b11d-466b-a756-092df2db0306">AVIStreamRead</a> function.




## -parameters




### -param lStart

Starting sample or frame number to read.


### -param lSamples

Number of samples to read.


### -param lpBuffer

Pointer to the application-defined buffer to contain the stream data. You can also specify <b>NULL</b> to request the required size of the buffer. Many applications precede each read operation with a query for the buffer size to see how large a buffer is needed.


### -param cbBuffer

Size, in bytes, of the buffer specified by <i>lpBuffer</i>.


### -param plBytes

Pointer to a buffer that receives the number of bytes read.


### -param plSamples

Pointer to a buffer that receives the number of samples read.


#### - ps

Pointer to the interface to a stream.


## -returns



Returns AVIERR_OK if successful or AVIERR_BUFFERTOOSMALL if the buffer is not large enough to hold the data. If successful, <b>Read</b> also returns either a buffer of data with the number of frames (samples) included in the buffer or the required buffer size, in bytes.




## -remarks



For handlers written in C++, <b>Read</b> has the following syntax:


```cpp

HRESULT Read(LONG lStart, LONG lSamples, 
    LPVOID lpBuffer, LONG cbBuffer, 
    LONG *plBytes, LONG *plSamples); 
 

```





## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

