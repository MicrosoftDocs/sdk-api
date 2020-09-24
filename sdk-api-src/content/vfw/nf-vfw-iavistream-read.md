---
UID: NF:vfw.IAVIStream.Read
title: IAVIStream::Read (vfw.h)
description: The Read method reads data from a stream and copies it to an application-defined buffer. If no buffer is supplied, it determines the buffer size needed to retrieve the next buffer of data. Called when an application uses the AVIStreamRead function.
helpviewer_keywords: ["IAVIStream interface [Windows Multimedia]","Read method","IAVIStream.Read","IAVIStream::Read","Read","Read method [Windows Multimedia]","Read method [Windows Multimedia]","IAVIStream interface","_win32_IAVIStream_Read","multimedia.iavistream_read","vfw/IAVIStream::Read"]
old-location: multimedia\iavistream_read.htm
tech.root: Multimedia
ms.assetid: 95835ba2-5085-467f-ae2c-27dd4d2ea68c
ms.date: 12/05/2018
ms.keywords: IAVIStream interface [Windows Multimedia],Read method, IAVIStream.Read, IAVIStream::Read, Read, Read method [Windows Multimedia], Read method [Windows Multimedia],IAVIStream interface, _win32_IAVIStream_Read, multimedia.iavistream_read, vfw/IAVIStream::Read
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAVIStream::Read
 - vfw/IAVIStream::Read
dev_langs:
 - c++
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
---

# IAVIStream::Read


## -description

The <b>Read</b> method reads data from a stream and copies it to an application-defined buffer. If no buffer is supplied, it determines the buffer size needed to retrieve the next buffer of data. Called when an application uses the <a href="/windows/desktop/api/vfw/nf-vfw-avistreamread">AVIStreamRead</a> function.

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

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>