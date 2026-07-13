---
UID: NC:evr.MFCreateVideoSampleFromSurface
title: MFCreateVideoSampleFromSurface (evr.h)
description: Creates a media sample that manages a Direct3D surface.
helpviewer_keywords: ["MFCreateVideoSampleFromSurface","MFCreateVideoSampleFromSurface callback","MFCreateVideoSampleFromSurface callback function [Media Foundation]","d34d423b-4510-44ce-ab46-51560b01f205","evr/MFCreateVideoSampleFromSurface","mf.mfcreatevideosamplefromsurface"]
old-location: mf\mfcreatevideosamplefromsurface.htm
tech.root: mfarchive
ms.assetid: d34d423b-4510-44ce-ab46-51560b01f205
ms.date: 12/05/2018
ms.keywords: MFCreateVideoSampleFromSurface, MFCreateVideoSampleFromSurface callback, MFCreateVideoSampleFromSurface callback function [Media Foundation], d34d423b-4510-44ce-ab46-51560b01f205, evr/MFCreateVideoSampleFromSurface, mf.mfcreatevideosamplefromsurface
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateVideoSampleFromSurface
 - evr/MFCreateVideoSampleFromSurface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - evr.dll
api_name:
 - MFCreateVideoSampleFromSurface
archived: true
ROBOTS: "INDEX,FOLLOW"
---

# MFCreateVideoSampleFromSurface callback function


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Creates a media sample that manages a Direct3D surface.

## -parameters

### -param pUnkSurface [in]

A pointer to the <b>IUnknown</b> interface of the Direct3D surface. This parameter can be <b>NULL</b>.

### -param ppSample [out]

Receives a pointer to the sample's <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> interface.
          The caller must release the interface.

## -returns

If this callback function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The media sample created by this function exposes the following interfaces in addition to <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a>:

<ul>
<li>
<a href="/windows/desktop/api/evr/nn-evr-imfdesiredsample">IMFDesiredSample</a>
</li>
<li>
<a href="/windows/desktop/api/mfidl/nn-mfidl-imftrackedsample">IMFTrackedSample</a>
</li>
</ul>
If <i>pUnkSurface</i> is non-<b>NULL</b>, the sample contains a single media buffer, which holds a pointer to the Direct3D surface. To get the Direct3D surface from the media buffer, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> on the buffer, using the service identifier MR_BUFFER_SERVICE. The media buffer does not implement <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a>, nor does it implement the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock">IMFMediaBuffer::Lock</a> and <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock">Unlock</a> methods.

Alternatively, you can set <i>pUnkSurface</i> to <b>NULL</b>, and later add a DirectX surface buffer to the sample by calling <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer">IMFSample::AddBuffer</a>. To create a DirectX surface buffer, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer">MFCreateDXSurfaceBuffer</a>.


#### Examples

The following example is taken from the <a href="/windows/desktop/medfound/evrpresenter-sample">EVRPresenter Sample</a>.


```cpp
//-----------------------------------------------------------------------------
// CreateD3DSample
//
// Creates a sample object (IMFSample) to hold a Direct3D swap chain.
//-----------------------------------------------------------------------------

HRESULT D3DPresentEngine::CreateD3DSample(
    IDirect3DSwapChain9 *pSwapChain,
    IMFSample **ppVideoSample
    )
{
    // Caller holds the object lock.

    D3DCOLOR clrBlack = D3DCOLOR_ARGB(0xFF, 0x00, 0x00, 0x00);

    IDirect3DSurface9* pSurface = NULL;
    IMFSample* pSample = NULL;

    // Get the back buffer surface.
    HRESULT hr = pSwapChain->GetBackBuffer(
        0, D3DBACKBUFFER_TYPE_MONO, &pSurface);
    if (FAILED(hr))
    {
        goto done;
    }

    // Fill it with black.
    hr = m_pDevice->ColorFill(pSurface, NULL, clrBlack);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the sample.
    hr = MFCreateVideoSampleFromSurface(pSurface, &pSample);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppVideoSample = pSample;
    (*ppVideoSample)->AddRef();

done:
    SafeRelease(&pSurface);
    SafeRelease(&pSample);
    return hr;
}

```

## -see-also

<a href="/windows/desktop/medfound/directx-surface-buffer">DirectX Surface Buffer</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-samples">Media Samples</a>