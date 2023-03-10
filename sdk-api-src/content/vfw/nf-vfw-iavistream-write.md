---
UID: NF:vfw.IAVIStream.Write
title: IAVIStream::Write (vfw.h)
description: The Write method writes data to a stream. Called when an application uses the AVIStreamWrite function.
helpviewer_keywords: ["IAVIStream interface [Windows Multimedia]","Write method","IAVIStream.Write","IAVIStream::Write","Write","Write method [Windows Multimedia]","Write method [Windows Multimedia]","IAVIStream interface","_win32_IAVIStream_Write","multimedia.iavistream_write","vfw/IAVIStream::Write"]
old-location: multimedia\iavistream_write.htm
tech.root: Multimedia
ms.assetid: 31252348-0830-4b1c-82a3-9f68818094da
ms.date: 12/05/2018
ms.keywords: IAVIStream interface [Windows Multimedia],Write method, IAVIStream.Write, IAVIStream::Write, Write, Write method [Windows Multimedia], Write method [Windows Multimedia],IAVIStream interface, _win32_IAVIStream_Write, multimedia.iavistream_write, vfw/IAVIStream::Write
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
 - IAVIStream::Write
 - vfw/IAVIStream::Write
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
 - IAVIStream.Write
---

# IAVIStream::Write


## -description

The <b>Write</b> method writes data to a stream. Called when an application uses the <a href="/windows/desktop/api/vfw/nf-vfw-avistreamwrite">AVIStreamWrite</a> function.

## -parameters

### -param lStart

Starting sample or frame number to write.

### -param lSamples

Number of samples to write.

### -param lpBuffer

Pointer to the buffer for the data.

### -param cbBuffer

Size, in bytes, of the buffer specified by <i>lpBuffer</i>.

### -param dwFlags

Applicable flags. The AVIF_KEYFRAME flag is defined and indicates that this frame contains all the information needed for a complete image.

### -param plSampWritten

Pointer to a buffer used to contain the number of samples written.

### -param plBytesWritten

Pointer to a buffer that receives the number of bytes written.


#### - ps

Pointer to the interface to a stream.

## -returns

Returns the HRESULT defined by OLE.

## -remarks

For handlers written in C++, <b>Write</b> has the following syntax:


```cpp

HRESULT Write(LONG lStart, LONG lSamples, LPVOID lpBuffer, 
    LONG cbBuffer, DWORD dwFlags, LONG *plSampWritten, 
    LONG *plBytesWritten); 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>