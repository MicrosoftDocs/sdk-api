---
UID: NF:vfw.IAVIEditStream.Cut
title: IAVIEditStream::Cut (vfw.h)
description: The Cut method removes a portion of a stream and places it in a temporary stream. Called when an application uses the EditStreamCut function.
helpviewer_keywords: ["Cut","Cut method [Windows Multimedia]","Cut method [Windows Multimedia]","IAVIEditStream interface","IAVIEditStream interface [Windows Multimedia]","Cut method","IAVIEditStream.Cut","IAVIEditStream::Cut","_win32_IAVIEditStream_Cut","multimedia.iavieditstream_cut","vfw/IAVIEditStream::Cut"]
old-location: multimedia\iavieditstream_cut.htm
tech.root: Multimedia
ms.assetid: e889d435-5c33-402d-bd69-c9122670e404
ms.date: 12/05/2018
ms.keywords: Cut, Cut method [Windows Multimedia], Cut method [Windows Multimedia],IAVIEditStream interface, IAVIEditStream interface [Windows Multimedia],Cut method, IAVIEditStream.Cut, IAVIEditStream::Cut, _win32_IAVIEditStream_Cut, multimedia.iavieditstream_cut, vfw/IAVIEditStream::Cut
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
 - IAVIEditStream::Cut
 - vfw/IAVIEditStream::Cut
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
 - IAVIEditStream.Cut
---

# IAVIEditStream::Cut


## -description

The <b>Cut</b> method removes a portion of a stream and places it in a temporary stream. Called when an application uses the <a href="/windows/desktop/api/vfw/nf-vfw-editstreamcut">EditStreamCut</a> function.

## -parameters

### -param plStart

Pointer to a buffer that receives the starting position of the operation.

### -param plLength

Pointer to a buffer that receives the length, in frames, of the operation.

### -param ppResult

Pointer to a buffer that receives a pointer to the interface to the new stream.


#### - pavi

Pointer to the interface to the stream to cut.

## -returns

Returns the HRESULT defined by OLE.

## -remarks

For handlers written in C++, <b>Cut</b> has the following syntax:


```cpp

HRESULT Cut(LONG *plStart, LONG *plLength, 
    PAVISTREAM *ppResult); 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>