---
UID: NF:vfw.IAVIEditStream.Paste
title: IAVIEditStream::Paste (vfw.h)
description: The Paste method copies a stream or a portion of it in another stream. Called when an application uses the EditStreamPaste function.
helpviewer_keywords: ["IAVIEditStream interface [Windows Multimedia]","Paste method","IAVIEditStream.Paste","IAVIEditStream::Paste","Paste","Paste method [Windows Multimedia]","Paste method [Windows Multimedia]","IAVIEditStream interface","_win32_IAVIEditStream_Paste","multimedia.iavieditstream_paste","vfw/IAVIEditStream::Paste"]
old-location: multimedia\iavieditstream_paste.htm
tech.root: Multimedia
ms.assetid: bdb6de96-6a1e-49ca-a824-ed6d7b43fd13
ms.date: 12/05/2018
ms.keywords: IAVIEditStream interface [Windows Multimedia],Paste method, IAVIEditStream.Paste, IAVIEditStream::Paste, Paste, Paste method [Windows Multimedia], Paste method [Windows Multimedia],IAVIEditStream interface, _win32_IAVIEditStream_Paste, multimedia.iavieditstream_paste, vfw/IAVIEditStream::Paste
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
 - IAVIEditStream::Paste
 - vfw/IAVIEditStream::Paste
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
 - IAVIEditStream.Paste
---

# IAVIEditStream::Paste


## -description

The <b>Paste</b> method copies a stream or a portion of it in another stream. Called when an application uses the <a href="/windows/desktop/api/vfw/nf-vfw-editstreampaste">EditStreamPaste</a> function.

## -parameters

### -param plPos

Pointer to a buffer that receives the starting position of the operation.

### -param plLength

Pointer to a buffer that receives the length, in bytes, of the data to paste from the source stream.

### -param pstream

Pointer to the interface to the source stream.

### -param lStart

Starting position of the copy operation within the source stream.

### -param lEnd

Ending position of the copy operation within the source stream.

## -returns

Returns the HRESULT defined by OLE.

## -remarks

For handlers written in C++, <b>Paste</b> has the following syntax:


```cpp

HRESULT Paste(LONG *plPos, LONG *plLength, 
    PAVISTREAM pstream, LONG lStart, LONG lLength); 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>