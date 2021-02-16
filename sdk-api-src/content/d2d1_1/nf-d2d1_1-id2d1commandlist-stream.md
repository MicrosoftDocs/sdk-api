---
UID: NF:d2d1_1.ID2D1CommandList.Stream
title: ID2D1CommandList::Stream (d2d1_1.h)
description: Streams the contents of the command list to the specified command sink.
helpviewer_keywords: ["ID2D1CommandList interface [Direct2D]","Stream method","ID2D1CommandList.Stream","ID2D1CommandList::Stream","Stream","Stream method [Direct2D]","Stream method [Direct2D]","ID2D1CommandList interface","d2d1_1/ID2D1CommandList::Stream","direct2d.id2d1commandlist_stream"]
old-location: direct2d\id2d1commandlist_stream.htm
tech.root: Direct2D
ms.assetid: 52e6da86-c7c6-48e7-b0ff-a54770663f14
ms.date: 12/05/2018
ms.keywords: ID2D1CommandList interface [Direct2D],Stream method, ID2D1CommandList.Stream, ID2D1CommandList::Stream, Stream, Stream method [Direct2D], Stream method [Direct2D],ID2D1CommandList interface, d2d1_1/ID2D1CommandList::Stream, direct2d.id2d1commandlist_stream
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1CommandList::Stream
 - d2d1_1/ID2D1CommandList::Stream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1CommandList.Stream
---

# ID2D1CommandList::Stream


## -description

Streams the contents of the command list  to the specified command sink.

## -parameters

### -param sink [in]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a>*</b>

The sink into which the command list will be streamed.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code. 


The return value indicates any failures the command sink implementation  returns through its <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-enddraw">EndDraw</a> method.

## -remarks

The command sink can be implemented by any caller of the API.

If the caller makes any design-time failure calls while a command list is selected as a target, the command list is placed in an error state. The stream call fails without making any calls to the passed in sink.

Sample use:


```cpp
Class MyCommandSink : public ID2D1CommandSink
{
public:
    // All of the ID2D1CommandSink methods implemented here.
};

HRESULT
StreamToMyCommandSink(
    __in ID2D1CommandList *pCommandList 
    )
{
    HRESULT hr = S_OK;
    
    MyCommandSink *pCommandSink = new MyCommandSink();
    hr = pCommandSink ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        // Receive the contents of the command sink streamed to the sink.
        hr = pCommandList->Stream(pCommandSink);
    }

    SafeRelease(&pCommandSink);
   
    return hr;

}
```

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandlist">ID2D1CommandList</a>