---
UID: NF:vfw.IAVIEditStream.Copy
title: IAVIEditStream::Copy (vfw.h)
description: The Copy method copies a stream or a portion of it to a temporary stream. Called when an application uses the EditStreamCopy function.
helpviewer_keywords: ["Copy","Copy method [Windows Multimedia]","Copy method [Windows Multimedia]","IAVIEditStream interface","IAVIEditStream interface [Windows Multimedia]","Copy method","IAVIEditStream.Copy","IAVIEditStream::Copy","_win32_IAVIEditStream_Copy","multimedia.iavieditstream_copy","vfw/IAVIEditStream::Copy"]
old-location: multimedia\iavieditstream_copy.htm
tech.root: Multimedia
ms.assetid: d2012d04-4fe5-4a49-8160-d27b7bc1bfc8
ms.date: 12/05/2018
ms.keywords: Copy, Copy method [Windows Multimedia], Copy method [Windows Multimedia],IAVIEditStream interface, IAVIEditStream interface [Windows Multimedia],Copy method, IAVIEditStream.Copy, IAVIEditStream::Copy, _win32_IAVIEditStream_Copy, multimedia.iavieditstream_copy, vfw/IAVIEditStream::Copy
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
 - IAVIEditStream::Copy
 - vfw/IAVIEditStream::Copy
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
 - IAVIEditStream.Copy
---

# IAVIEditStream::Copy


## -description

The <b>Copy</b> method copies a stream or a portion of it to a temporary stream. Called when an application uses the <a href="/windows/desktop/api/vfw/nf-vfw-editstreamcopy">EditStreamCopy</a> function.

## -parameters

### -param plStart

Pointer to a buffer that receives the starting position of the operation.

### -param plLength

Pointer to a buffer that receives the length, in frames, of the operation.

### -param ppResult

Pointer to a buffer that receives a pointer to the interface to the new stream.


#### - pavi

Pointer to the interface to the stream to copy.

## -returns

Returns the HRESULT defined by OLE.

## -remarks

For handlers written in C++, <b>Copy</b> has the following syntax:


```cpp

HRESULT Copy(LONG *plStart, LONG *plLength, 
    PAVISTREAM * ppResult); 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>