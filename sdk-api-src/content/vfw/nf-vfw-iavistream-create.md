---
UID: NF:vfw.IAVIStream.Create
title: IAVIStream::Create (vfw.h)
description: The Create method initializes a stream handler that is not associated with any file. Called when an application uses the AVIStreamCreate function.
helpviewer_keywords: ["Create","Create method [Windows Multimedia]","Create method [Windows Multimedia]","IAVIStream interface","IAVIStream interface [Windows Multimedia]","Create method","IAVIStream.Create","IAVIStream::Create","_win32_IAVIStream_Create","multimedia.iavistream_create","vfw/IAVIStream::Create"]
old-location: multimedia\iavistream_create.htm
tech.root: Multimedia
ms.assetid: 512ce9f8-f96c-4ef4-be1f-234165219ff7
ms.date: 12/05/2018
ms.keywords: Create, Create method [Windows Multimedia], Create method [Windows Multimedia],IAVIStream interface, IAVIStream interface [Windows Multimedia],Create method, IAVIStream.Create, IAVIStream::Create, _win32_IAVIStream_Create, multimedia.iavistream_create, vfw/IAVIStream::Create
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
 - IAVIStream::Create
 - vfw/IAVIStream::Create
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
 - IAVIStream.Create
---

# IAVIStream::Create


## -description

The <b>Create</b> method initializes a stream handler that is not associated with any file. Called when an application uses the <a href="/windows/desktop/api/vfw/nf-vfw-avistreamcreate">AVIStreamCreate</a> function.

## -parameters

### -param lParam1

Stream handler-specific data.

### -param lParam2

Stream handler-specific data.


#### - ps

Pointer to the interface to a stream.

## -returns

Returns the HRESULT defined by OLE.

## -remarks

For handlers written in C++, <b>Create</b> has the following syntax:


```cpp

HRESULT Create(LONG lParam1, LONG lParam2) 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>