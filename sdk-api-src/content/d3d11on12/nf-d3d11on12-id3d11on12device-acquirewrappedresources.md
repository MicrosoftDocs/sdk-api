---
UID: NF:d3d11on12.ID3D11On12Device.AcquireWrappedResources
title: ID3D11On12Device::AcquireWrappedResources (d3d11on12.h)
author: windows-sdk-content
description: Acquires D3D11 resources for use with D3D 11on12. Indicates that rendering to the wrapped resources can begin again.
old-location: direct3d12\id3d11on12device_acquirewrappedresources.htm
tech.root: direct3d12
ms.assetid: 123FC8D9-6411-4CB7-921B-CEB32F5A9AD9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AcquireWrappedResources, AcquireWrappedResources method, AcquireWrappedResources method,ID3D11On12Device interface, ID3D11On12Device interface,AcquireWrappedResources method, ID3D11On12Device.AcquireWrappedResources, ID3D11On12Device::AcquireWrappedResources, d3d11on12/ID3D11On12Device::AcquireWrappedResources, direct3d12.id3d11on12device_acquirewrappedresources
ms.topic: method
f1_keywords: ["d3d11on12/ID3D11On12Device.AcquireWrappedResources"]
req.header: d3d11on12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: D3D11.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.dll
api_name:
 - ID3D11On12Device.AcquireWrappedResources
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11On12Device::AcquireWrappedResources


## -description


Acquires D3D11 resources for use with D3D 11on12.
          Indicates that rendering to the wrapped resources can begin again.
        


## -parameters




### -param ppResources [in]

Type: <b>ID3D11Resource*</b>

Specifies a pointer to a set of D3D11 resources, defined by <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>.
          


### -param NumResources

Type: <b>UINT</b>

Count of the number of resources.
          


## -returns



This method does not return a value.
          




## -remarks



This method marks the resources as "acquired" in hazard tracking.
        

Keyed mutex resources cannot be provided to this method; use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgikeyedmutex-acquiresync">IDXGIKeyedMutex::AcquireSync</a> instead.
        


#### Examples

Render text over D3D12 using D2D via the 11On12 device.


```cpp
// Render text over D3D12 using D2D via the 11On12 device.
void D3D1211on12::RenderUI()
{
    D2D1_SIZE_F rtSize = m_d2dRenderTargets[m_frameIndex]->GetSize();
    D2D1_RECT_F textRect = D2D1::RectF(0, 0, rtSize.width, rtSize.height);
    static const WCHAR text[] = L"11On12";

    // Acquire our wrapped render target resource for the current back buffer.
    m_d3d11On12Device->AcquireWrappedResources(m_wrappedBackBuffers[m_frameIndex].GetAddressOf(), 1);

    // Render text directly to the back buffer.
    m_d2dDeviceContext->SetTarget(m_d2dRenderTargets[m_frameIndex].Get());
    m_d2dDeviceContext->BeginDraw();
    m_d2dDeviceContext->SetTransform(D2D1::Matrix3x2F::Identity());
    m_d2dDeviceContext->DrawTextW(
        text,
        _countof(text) - 1,
        m_textFormat.Get(),
        &textRect,
        m_textBrush.Get()
        );
    ThrowIfFailed(m_d2dDeviceContext->EndDraw());

    // Release our wrapped render target resource. Releasing 
    // transitions the back buffer resource to the state specified
    // as the OutState when the wrapped resource was created.
    m_d3d11On12Device->ReleaseWrappedResources(m_wrappedBackBuffers[m_frameIndex].GetAddressOf(), 1);

    // Flush to submit the 11 command list to the shared command queue.
    m_d3d11DeviceContext->Flush();
}

```


Refer to the <a href="https://docs.microsoft.com/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device">ID3D11On12Device</a>
 

 

