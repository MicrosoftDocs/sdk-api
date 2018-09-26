---
UID: NF:d3d11on12.ID3D11On12Device.ReleaseWrappedResources
title: ID3D11On12Device::ReleaseWrappedResources
author: windows-sdk-content
description: Releases D3D11 resources that were wrapped for D3D 11on12.
old-location: direct3d12\id3d11on12device_releasewrappedresources.htm
tech.root: direct3d12
ms.assetid: 6591D7D4-9B8D-4837-9DCF-0502CC26E725
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: ID3D11On12Device interface,ReleaseWrappedResources method, ID3D11On12Device.ReleaseWrappedResources, ID3D11On12Device::ReleaseWrappedResources, ReleaseWrappedResources, ReleaseWrappedResources method, ReleaseWrappedResources method,ID3D11On12Device interface, d3d11on12/ID3D11On12Device::ReleaseWrappedResources, direct3d12.id3d11on12device_releasewrappedresources
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ID3D11On12Device.ReleaseWrappedResources
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11On12Device::ReleaseWrappedResources


## -description


Releases D3D11 resources that were wrapped for D3D 11on12.
        


## -parameters




### -param ppResources [in]

Type: <b>ID3D11Resource*</b>

Specifies a pointer to a set of D3D11 resources, defined by <a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>.
          


### -param NumResources

Type: <b>UINT</b>

Count of the number of resources.
          


## -returns



This method does not return a value.
          




## -remarks



Call this method prior to calling Flush, to insert resource barriers to the appropriate "out" state, and to mark that they should then be expected to be in the "in" state.
          If no resource list is provided, all wrapped resources are transitioned.
          These resources will be marked as “not acquired” in hazard tracking until <a href="https://msdn.microsoft.com/123FC8D9-6411-4CB7-921B-CEB32F5A9AD9">ID3D11On12Device::AcquireWrappedResources</a> is called.
        

Keyed mutex resources cannot be provided to this method; use <a href="https://msdn.microsoft.com/324741c9-33f2-4420-8c3f-4984e2ca0962">IDXGIKeyedMutex::ReleaseSync</a> instead.
        


#### Examples

Render text over D3D12 using D2D via the 11On12 device.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Render text over D3D12 using D2D via the 11On12 device.
void D3D1211on12::RenderUI()
{
    D2D1_SIZE_F rtSize = m_d2dRenderTargets[m_frameIndex]-&gt;GetSize();
    D2D1_RECT_F textRect = D2D1::RectF(0, 0, rtSize.width, rtSize.height);
    static const WCHAR text[] = L"11On12";

    // Acquire our wrapped render target resource for the current back buffer.
    m_d3d11On12Device-&gt;AcquireWrappedResources(m_wrappedBackBuffers[m_frameIndex].GetAddressOf(), 1);

    // Render text directly to the back buffer.
    m_d2dDeviceContext-&gt;SetTarget(m_d2dRenderTargets[m_frameIndex].Get());
    m_d2dDeviceContext-&gt;BeginDraw();
    m_d2dDeviceContext-&gt;SetTransform(D2D1::Matrix3x2F::Identity());
    m_d2dDeviceContext-&gt;DrawTextW(
        text,
        _countof(text) - 1,
        m_textFormat.Get(),
        &amp;textRect,
        m_textBrush.Get()
        );
    ThrowIfFailed(m_d2dDeviceContext-&gt;EndDraw());

    // Release our wrapped render target resource. Releasing 
    // transitions the back buffer resource to the state specified
    // as the OutState when the wrapped resource was created.
    m_d3d11On12Device-&gt;ReleaseWrappedResources(m_wrappedBackBuffers[m_frameIndex].GetAddressOf(), 1);

    // Flush to submit the 11 command list to the shared command queue.
    m_d3d11DeviceContext-&gt;Flush();
}
</pre>
</td>
</tr>
</table></span></div>
Refer to the <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/031F9AC2-E5C0-47F9-B084-2D2431F1187A">ID3D11On12Device</a>
 

 

