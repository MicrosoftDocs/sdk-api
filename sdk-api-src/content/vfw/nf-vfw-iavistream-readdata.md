---
UID: NF:vfw.IAVIStream.ReadData
title: IAVIStream::ReadData (vfw.h)
description: The ReadData method reads data headers of a stream. Called when an application uses the AVIStreamReadData function.
helpviewer_keywords: ["IAVIStream interface [Windows Multimedia]","ReadData method","IAVIStream.ReadData","IAVIStream::ReadData","ReadData","ReadData method [Windows Multimedia]","ReadData method [Windows Multimedia]","IAVIStream interface","_win32_IAVIStream_ReadData","multimedia.iavistream_readdata","vfw/IAVIStream::ReadData"]
old-location: multimedia\iavistream_readdata.htm
tech.root: Multimedia
ms.assetid: 688a19fb-5774-4e05-b0e8-4a98922def89
ms.date: 12/05/2018
ms.keywords: IAVIStream interface [Windows Multimedia],ReadData method, IAVIStream.ReadData, IAVIStream::ReadData, ReadData, ReadData method [Windows Multimedia], ReadData method [Windows Multimedia],IAVIStream interface, _win32_IAVIStream_ReadData, multimedia.iavistream_readdata, vfw/IAVIStream::ReadData
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
 - IAVIStream::ReadData
 - vfw/IAVIStream::ReadData
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
 - IAVIStream.ReadData
---

# IAVIStream::ReadData


## -description

The <b>ReadData</b> method reads data headers of a stream. Called when an application uses the <a href="/windows/desktop/api/vfw/nf-vfw-avistreamreaddata">AVIStreamReadData</a> function.

## -parameters

### -param fcc

Four-character code of the stream header to read.

### -param lp

Pointer to the buffer to contain the header data.

### -param lpcb

Size, in bytes, of the buffer specified by <i>lpBuffer</i>. When this method returns control to the application, the contents of this parameter specifies the amount of data read.

## -returns

Returns the HRESULT defined by OLE.

## -remarks

For handlers written in C++, <b>ReadData</b> has the following syntax:


```cpp

HRESULT ReadData(DWORD fcc, LPVOID lp, LONG *lpcb); 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>