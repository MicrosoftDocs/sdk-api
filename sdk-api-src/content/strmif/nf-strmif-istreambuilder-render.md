---
UID: NF:strmif.IStreamBuilder.Render
title: IStreamBuilder::Render (strmif.h)
description: The Render method completes rendering of the stream originating with this pin. This can involve adding filters to the filter graph and connecting them.
helpviewer_keywords: ["IStreamBuilder interface [DirectShow]","Render method","IStreamBuilder.Render","IStreamBuilder::Render","IStreamBuilderRender","Render","Render method [DirectShow]","Render method [DirectShow]","IStreamBuilder interface","dshow.istreambuilder_render","strmif/IStreamBuilder::Render"]
old-location: dshow\istreambuilder_render.htm
tech.root: dshow
ms.assetid: 7bba9d1a-03a8-4572-a08c-2e12071df73b
ms.date: 4/26/2023
ms.keywords: IStreamBuilder interface [DirectShow],Render method, IStreamBuilder.Render, IStreamBuilder::Render, IStreamBuilderRender, Render, Render method [DirectShow], Render method [DirectShow],IStreamBuilder interface, dshow.istreambuilder_render, strmif/IStreamBuilder::Render
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
 - IStreamBuilder::Render
 - strmif/IStreamBuilder::Render
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
 - IStreamBuilder.Render
---

# IStreamBuilder::Render


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Render</code> method completes rendering of the stream originating with this pin. This can involve adding filters to the filter graph and connecting them.

## -parameters

### -param ppinOut [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface of this pin.

### -param pGraph [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> interface of the Filter Graph Manager.

## -returns

Returns an <b>HRESULT</b> value. A return code of S_OK indicates that the stream was successfully rendered.

## -remarks

The following code illustrates how to implement this method on an output pin. This example assumes that the filter requires a custom renderer downstream from it.

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>

```
STDMETHODIMP CMyOutputPin::Render(IPin *pPin, IGraphBuilder *pGraph)
{
    CheckPointer(pPin, E_POINTER);
    CheckPointer(pGraph, E_POINTER);

    // This filter needs a special renderer connected to it.
    IBaseFilter *pMyRenderer = NULL;

    // Create the renderer.
    HRESULT hr = CoCreateInstance(CLSID_MyRenderer, NULL, CLSCTX_INPROC,
        IID_IBaseFilter, (void **)&pMyRenderer);
    if (FAILED(hr))
    {
        return hr;
    }
    
    // Add my renderer to the filter graph.
    hr = pGraph->AddFilter(pMyRenderer, L"My Renderer");
    if (FAILED(hr))
    {
        pMyRenderer->Release();
        return hr;
    }

    IEnumPins *pEnumPins;
    IPin *pMyRendererInputPin = NULL;
    hr = pMyRenderer->EnumPins(&pEnumPins);
    if (SUCCEEDED(hr)) 
    {
        if (S_OK != pEnumPins->Next(1, &pMyRendererInputPin, 0))
        {
            hr = E_UNEXPECTED;
         }
    }
    if (SUCCEEDED(hr)) 
    {
        // Connect my renderer to my output pin.
        hr = pGraph->ConnectDirect(pPin, pMyRendererInputPin);
        pMyRendererInputPin->Release();
    }
    if (FAILED(hr)) 
    {
        // Could not connect to my renderer. Remove it from the graph.
        pGraph->RemoveFilter(pMyRenderer);
    }
    pMyRenderer->Release();
    return hr;
}
```
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-istreambuilder">IStreamBuilder Interface</a>