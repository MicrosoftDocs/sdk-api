---
UID: NC:evr.MFCreateVideoSampleFromSurface
title: MFCreateVideoSampleFromSurface
author: windows-sdk-content
description: Creates a media sample that manages a Direct3D surface.
old-location: mf\mfcreatevideosamplefromsurface.htm
old-project: medfound
ms.assetid: d34d423b-4510-44ce-ab46-51560b01f205
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: MFCreateVideoSampleFromSurface, MFCreateVideoSampleFromSurface callback, MFCreateVideoSampleFromSurface callback function [Media Foundation], d34d423b-4510-44ce-ab46-51560b01f205, evr/MFCreateVideoSampleFromSurface, mf.mfcreatevideosamplefromsurface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: EVENT_FILTER_LEVEL_KW, *PEVENT_FILTER_LEVEL_KW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - evr.h
api_name:
 - MFCreateVideoSampleFromSurface
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# MFCreateVideoSampleFromSurface callback function


## -description



          Creates a media sample that manages a Direct3D surface.
        


## -parameters




### -param pUnkSurface [in]


            A pointer to the <b>IUnknown</b> interface of the Direct3D surface. This parameter can be <b>NULL</b>.
          


### -param ppSample [out]


            Receives a pointer to the sample's <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> interface.
          The caller must release the interface.


## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The media sample created by this function exposes the following interfaces in addition to <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a>:

<ul>
<li>
<a href="https://msdn.microsoft.com/373c076c-6329-4332-9f07-f18a01197659">IMFDesiredSample</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4ad4b14c-94af-4314-8a16-163579dec67f">IMFTrackedSample</a>
</li>
</ul>
If <i>pUnkSurface</i> is non-<b>NULL</b>, the sample contains a single media buffer, which holds a pointer to the Direct3D surface. To get the Direct3D surface from the media buffer, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> on the buffer, using the service identifier MR_BUFFER_SERVICE. The media buffer does not implement <a href="https://msdn.microsoft.com/80eb23db-a7c0-4dbe-97d8-0dc07a34d8f7">IMF2DBuffer</a>, nor does it implement the <a href="https://msdn.microsoft.com/28ac372a-6e73-4e66-bf69-bcc244821b71">IMFMediaBuffer::Lock</a> and <a href="https://msdn.microsoft.com/3ca53321-5533-45f0-b415-6a16f780ec54">Unlock</a> methods.

Alternatively, you can set <i>pUnkSurface</i> to <b>NULL</b>, and later add a DirectX surface buffer to the sample by calling <a href="https://msdn.microsoft.com/61c2a1dc-b9fe-4296-bf33-d54006cad32b">IMFSample::AddBuffer</a>. To create a DirectX surface buffer, call <a href="https://msdn.microsoft.com/d1ee158e-5d70-41a4-b746-2ecaea2db92c">MFCreateDXSurfaceBuffer</a>.


#### Examples

The following example is taken from the <a href="https://msdn.microsoft.com/791a9816-4c40-4683-8b32-22f73d7fe84d">EVRPresenter Sample</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//-----------------------------------------------------------------------------
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
    HRESULT hr = pSwapChain-&gt;GetBackBuffer(
        0, D3DBACKBUFFER_TYPE_MONO, &amp;pSurface);
    if (FAILED(hr))
    {
        goto done;
    }

    // Fill it with black.
    hr = m_pDevice-&gt;ColorFill(pSurface, NULL, clrBlack);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the sample.
    hr = MFCreateVideoSampleFromSurface(pSurface, &amp;pSample);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppVideoSample = pSample;
    (*ppVideoSample)-&gt;AddRef();

done:
    SafeRelease(&amp;pSurface);
    SafeRelease(&amp;pSample);
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/2c82c023-4436-4f8a-b896-7f4765f989b3">DirectX Surface Buffer</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/14389eea-8091-4c10-849e-53db3e98a7c8">Media Samples</a>
 

 

