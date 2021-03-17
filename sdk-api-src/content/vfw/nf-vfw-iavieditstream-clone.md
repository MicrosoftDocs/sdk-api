---
UID: NF:vfw.IAVIEditStream.Clone
title: IAVIEditStream::Clone (vfw.h)
description: The Clone method duplicates a stream. Called when an application uses the EditStreamClone function.
helpviewer_keywords: ["Clone","Clone method [Windows Multimedia]","Clone method [Windows Multimedia]","IAVIEditStream interface","IAVIEditStream interface [Windows Multimedia]","Clone method","IAVIEditStream.Clone","IAVIEditStream::Clone","_win32_IAVIEditStream_Clone","multimedia.iavieditstream_clone","vfw/IAVIEditStream::Clone"]
old-location: multimedia\iavieditstream_clone.htm
tech.root: Multimedia
ms.assetid: 7112056e-5e25-4262-abe3-5cbb0675a475
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Multimedia], Clone method [Windows Multimedia],IAVIEditStream interface, IAVIEditStream interface [Windows Multimedia],Clone method, IAVIEditStream.Clone, IAVIEditStream::Clone, _win32_IAVIEditStream_Clone, multimedia.iavieditstream_clone, vfw/IAVIEditStream::Clone
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
 - IAVIEditStream::Clone
 - vfw/IAVIEditStream::Clone
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
 - IAVIEditStream.Clone
---

# IAVIEditStream::Clone


## -description

The <b>Clone</b> method duplicates a stream. Called when an application uses the <a href="/windows/desktop/api/vfw/nf-vfw-editstreamclone">EditStreamClone</a> function.

## -parameters

### -param ppResult

Pointer to a buffer that receives a pointer to the interface to the new stream.


#### - pavi

Pointer to the interface to the stream being cloned.

## -returns

The method returns the HRESULT defined by OLE.

## -remarks

For handlers written in C++, <b>Clone</b> has the following syntax:


```cpp

HRESULT Clone(PAVISTREAM *ppResult); 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>