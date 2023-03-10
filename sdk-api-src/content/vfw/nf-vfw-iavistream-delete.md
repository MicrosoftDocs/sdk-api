---
UID: NF:vfw.IAVIStream.Delete
title: IAVIStream::Delete (vfw.h)
description: The Delete method deletes data from a stream.
helpviewer_keywords: ["Delete","Delete method [Windows Multimedia]","Delete method [Windows Multimedia]","IAVIStream interface","IAVIStream interface [Windows Multimedia]","Delete method","IAVIStream.Delete","IAVIStream::Delete","_win32_IAVIStream_Delete","multimedia.iavistream_delete","vfw/IAVIStream::Delete"]
old-location: multimedia\iavistream_delete.htm
tech.root: Multimedia
ms.assetid: 0872023e-a760-4080-99da-df2941b84611
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [Windows Multimedia], Delete method [Windows Multimedia],IAVIStream interface, IAVIStream interface [Windows Multimedia],Delete method, IAVIStream.Delete, IAVIStream::Delete, _win32_IAVIStream_Delete, multimedia.iavistream_delete, vfw/IAVIStream::Delete
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
 - IAVIStream::Delete
 - vfw/IAVIStream::Delete
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
 - IAVIStream.Delete
---

# IAVIStream::Delete


## -description

The <b>Delete</b> method deletes data from a stream.

## -parameters

### -param lStart

Starting sample or frame number to delete.

### -param lSamples

Number of samples to delete.


#### - ps

Pointer to the interface to a stream.

## -returns

Returns the HRESULT defined by OLE.

## -remarks

For handlers written in C++, <b>Delete</b> has the following syntax:


```cpp

HRESULT Delete(LONG lStart, LONG lSamples); 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>