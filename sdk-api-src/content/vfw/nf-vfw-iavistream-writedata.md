---
UID: NF:vfw.IAVIStream.WriteData
title: IAVIStream::WriteData (vfw.h)
description: The WriteData method writes headers for a stream. Called when an application uses the AVIStreamWriteData function.
helpviewer_keywords: ["IAVIStream interface [Windows Multimedia]","WriteData method","IAVIStream.WriteData","IAVIStream::WriteData","WriteData","WriteData method [Windows Multimedia]","WriteData method [Windows Multimedia]","IAVIStream interface","_win32_IAVIStream_WriteData","multimedia.iavistream_writedata","vfw/IAVIStream::WriteData"]
old-location: multimedia\iavistream_writedata.htm
tech.root: Multimedia
ms.assetid: b6fb8e25-b6f9-4134-bb63-0a96fea88db8
ms.date: 12/05/2018
ms.keywords: IAVIStream interface [Windows Multimedia],WriteData method, IAVIStream.WriteData, IAVIStream::WriteData, WriteData, WriteData method [Windows Multimedia], WriteData method [Windows Multimedia],IAVIStream interface, _win32_IAVIStream_WriteData, multimedia.iavistream_writedata, vfw/IAVIStream::WriteData
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
 - IAVIStream::WriteData
 - vfw/IAVIStream::WriteData
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
 - IAVIStream.WriteData
---

# IAVIStream::WriteData


## -description

The <b>WriteData</b> method writes headers for a stream. Called when an application uses the <a href="/windows/desktop/api/vfw/nf-vfw-avistreamwritedata">AVIStreamWriteData</a> function.

## -parameters

### -param fcc

Four-character code of the stream header to write.

### -param lp

Pointer to the buffer that contains the header data to write.

### -param cb

Size, in bytes, of the buffer specified by <i>lpBuffer</i>.

## -returns

Returns the HRESULT defined by OLE.

## -remarks

For handlers written in C++, <b>WriteData</b> has the following syntax:


```cpp

HRESULT WriteData(DWORD fcc, LPVOID lpBuffer, LONG cbBuffer); 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>