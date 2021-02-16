---
UID: NF:strmif.IFilterGraph2.RenderEx
title: IFilterGraph2::RenderEx (strmif.h)
description: The RenderEx method renders an output pin, with an option to use existing renderers only.
helpviewer_keywords: ["IFilterGraph2 interface [DirectShow]","RenderEx method","IFilterGraph2.RenderEx","IFilterGraph2::RenderEx","IFilterGraph2RenderEx","RenderEx","RenderEx method [DirectShow]","RenderEx method [DirectShow]","IFilterGraph2 interface","dshow.ifiltergraph2_renderex","strmif/IFilterGraph2::RenderEx"]
old-location: dshow\ifiltergraph2_renderex.htm
tech.root: dshow
ms.assetid: b169c784-2ce3-47dc-ad64-3e4c96483f34
ms.date: 12/05/2018
ms.keywords: IFilterGraph2 interface [DirectShow],RenderEx method, IFilterGraph2.RenderEx, IFilterGraph2::RenderEx, IFilterGraph2RenderEx, RenderEx, RenderEx method [DirectShow], RenderEx method [DirectShow],IFilterGraph2 interface, dshow.ifiltergraph2_renderex, strmif/IFilterGraph2::RenderEx
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFilterGraph2::RenderEx
 - strmif/IFilterGraph2::RenderEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFilterGraph2.RenderEx
---

# IFilterGraph2::RenderEx


## -description

The <code>RenderEx</code> method renders an output pin, with an option to use existing renderers only.

## -parameters

### -param pPinOut [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface of the output pin.

### -param dwFlags [in]

Flag that specifies how to render the pin. If the value is AM_RENDEREX_RENDERTOEXISTINGRENDERERS, the method attempts to use renderers already in the filter graph. It will not add new renderers to the graph. (It will add intermediate transform filters, if needed.) For the method to succeed, the graph must contain the appropriate renderers, and they must have unconnected input pins. If the value is zero, the method behaves identically to the <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-render">IGraphBuilder::Render</a> method.

### -param pvContext [in, out]

Reserved. Must be <b>NULL</b>.

## -returns

Returns an <b>HRESULT</b>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph2">IFilterGraph2 Interface</a>