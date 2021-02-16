---
UID: NF:vfw.IAVIStream.SetFormat
title: IAVIStream::SetFormat (vfw.h)
description: The SetFormat method sets format information in a stream. Called when an application uses the AVIStreamSetFormat function.
helpviewer_keywords: ["IAVIStream interface [Windows Multimedia]","SetFormat method","IAVIStream.SetFormat","IAVIStream::SetFormat","SetFormat","SetFormat method [Windows Multimedia]","SetFormat method [Windows Multimedia]","IAVIStream interface","_win32_IAVIStream_SetFormat","multimedia.iavistream_setformat","vfw/IAVIStream::SetFormat"]
old-location: multimedia\iavistream_setformat.htm
tech.root: Multimedia
ms.assetid: 8693ce01-1f73-4d1b-ba8a-12f6453def22
ms.date: 12/05/2018
ms.keywords: IAVIStream interface [Windows Multimedia],SetFormat method, IAVIStream.SetFormat, IAVIStream::SetFormat, SetFormat, SetFormat method [Windows Multimedia], SetFormat method [Windows Multimedia],IAVIStream interface, _win32_IAVIStream_SetFormat, multimedia.iavistream_setformat, vfw/IAVIStream::SetFormat
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
 - IAVIStream::SetFormat
 - vfw/IAVIStream::SetFormat
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
 - IAVIStream.SetFormat
---

# IAVIStream::SetFormat


## -description

The <b>SetFormat</b> method sets format information in a stream. Called when an application uses the <a href="/windows/desktop/api/vfw/nf-vfw-avistreamsetformat">AVIStreamSetFormat</a> function.

## -parameters

### -param lPos

Pointer to the interface to a stream.

### -param lpFormat

Pointer to the buffer for the format data.

### -param cbFormat

Address containing the size, in bytes, of the buffer specified by <i>lpFormat</i>.

## -returns

Returns the HRESULT defined by OLE.

## -remarks

Standard video stream handlers provide format information in a <b>BITMAPINFOHEADER</b> structure. Standard audio stream handlers provide format information in a <b>PCMWAVEFORMAT</b> structure. Other data streams can use other structures that describe the stream data.

For handlers written in C++, <b>SetFormat</b> has the following syntax:


```cpp

HRESULT SetFormat(LONG lPos, LPVOID lpFormat, LONG cbFormat) 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>