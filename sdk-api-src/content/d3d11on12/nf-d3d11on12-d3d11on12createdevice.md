---
UID: NF:d3d11on12.D3D11On12CreateDevice
title: D3D11On12CreateDevice function
author: windows-sdk-content
description: Creates a device that uses Direct3D 11 functionality in Direct3D 12, specifying a pre-existing D3D12 device to use for D3D11 interop.
old-location: direct3d12\d3d11on12createdevice.htm
tech.root: direct3d12
ms.assetid: 6FC2CB44-4AA8-4E89-9E9B-ED1C3C9C64CC
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: D3D11On12CreateDevice, D3D11On12CreateDevice function, d3d11on12/D3D11On12CreateDevice, direct3d12.d3d11on12createdevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - DllExport
api_location:
 - D3D11.dll
api_name:
 - D3D11On12CreateDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D3D11On12CreateDevice function


## -description


Creates a device that uses Direct3D 11 functionality in Direct3D 12, specifying a pre-existing D3D12 device to use for D3D11 interop.
        


## -parameters




### -param pDevice [in]

Type: <b>IUnknown*</b>

Specifies a pre-existing D3D12 device to use for D3D11 interop.
            May not be NULL.
          


### -param Flags

Type: <b>UINT</b>

One or more bitwise OR'ed flags from <a href="https://msdn.microsoft.com/en-us/library/Ff476107(v=VS.85).aspx">D3D11_CREATE_DEVICE_FLAG</a>. These are the same flags as those used by <a href="https://msdn.microsoft.com/en-us/library/Ff476083(v=VS.85).aspx">D3D11CreateDeviceAndSwapChain</a>.
            Specifies which runtime <a href="https://msdn.microsoft.com/en-us/library/Ff476881(v=VS.85).aspx">layers</a> to enable.
            <i>Flags</i> must be compatible with device flags, and its <i>NodeMask</i> must be a subset of the <i>NodeMask</i> provided to the present API.
          


### -param pFeatureLevels [in, optional]

Type: <b>const D3D_FEATURE_LEVEL*</b>

An array of any of the following:
            

<ul>
<li>D3D_FEATURE_LEVEL_12_1</li>
<li>D3D_FEATURE_LEVEL_12_0</li>
<li>D3D_FEATURE_LEVEL_11_1</li>
<li>D3D_FEATURE_LEVEL_11_0</li>
<li>D3D_FEATURE_LEVEL_10_1</li>
<li>D3D_FEATURE_LEVEL_10_0</li>
<li>D3D_FEATURE_LEVEL_9_3</li>
<li>D3D_FEATURE_LEVEL_9_2</li>
<li>D3D_FEATURE_LEVEL_9_1</li>
</ul>
The first feature level which is less than or equal to the
              D3D12 device's feature level will be used to perform D3D11 validation.
              Creation will fail if no acceptable feature levels are provided.
              Providing NULL will default to the D3D12 device's feature level.
            


### -param FeatureLevels

Type: <b>UINT</b>

The size of the feature levels array, in bytes.
          


### -param ppCommandQueues [in, optional]

Type: <b>IUnknown*</b>

An array of unique queues for D3D11On12 to use.
            Valid queue types: 3D command queue.
          


### -param NumQueues

Type: <b>UINT</b>

The size of the command queue array, in bytes.
          


### -param NodeMask

Type: <b>UINT</b>

Which node of the D3D12 device to use.
            Only 1 bit may be set.
          


### -param ppDevice [out, optional]

Type: <b>ID3D11Device**</b>

Pointer to the returned
            <a href="https://msdn.microsoft.com/en-us/library/Ff476379(v=VS.85).aspx">ID3D11Device</a>.
            May be NULL.
          


### -param ppImmediateContext [out, optional]

Type: <b>ID3D11DeviceContext**</b>

A pointer to the returned
            <a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a>.
            May be NULL.
          


### -param pChosenFeatureLevel [out, optional]

Type: <b>D3D_FEATURE_LEVEL*</b>

A pointer to the returned feature level.
            May be NULL.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/en-us/library/Dn706075(v=VS.85).aspx">Direct3D 12 Return Codes</a> that are documented for
            <a href="https://msdn.microsoft.com/en-us/library/Ff476082(v=VS.85).aspx">D3D11CreateDevice</a>.
            See Direct3D 12 Return Codes.
          

This method returns <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR_SDK_COMPONENT_MISSING</a>if you specify <a href="https://msdn.microsoft.com/en-us/library/Ff476107(v=VS.85).aspx">D3D11_CREATE_DEVICE_DEBUG</a>in <i>Flags</i>and the incorrect version of the <a href="https://msdn.microsoft.com/en-us/library/Ff476881(v=VS.85).aspx">debug layer</a> is installed on your computer.
            Install the latest Windows SDK to get the correct version.
          




## -remarks



The function signature PFN_D3D11ON12_CREATE_DEVICE is provided as a typedef, so that you can use dynamic linking techniques (<a href="https://msdn.microsoft.com/library/windows/desktop/ms683212(v=vs.85).aspx">GetProcAddress</a>) instead of statically linking.
      


#### Examples

To render text over D3D12 using D2D via the 11On12 device, load the rendering pipeline dependencies.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Load the rendering pipeline dependencies.
void D3D1211on12::LoadPipeline()
{
    UINT d3d11DeviceFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
    D2D1_FACTORY_OPTIONS d2dFactoryOptions = {};
#if defined(_DEBUG)
    // Enable the D2D debug layer.
    d2dFactoryOptions.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;

    // Enable the D3D11 debug layer.
    d3d11DeviceFlags |= D3D11_CREATE_DEVICE_DEBUG;
    
    // Enable the D3D12 debug layer.
    {
        ComPtr&lt;ID3D12Debug&gt; debugController;
        if (SUCCEEDED(D3D12GetDebugInterface(IID_PPV_ARGS(&amp;debugController))))
        {
            debugController-&gt;EnableDebugLayer();
        }
    }
#endif

    ComPtr&lt;IDXGIFactory4&gt; factory;
    ThrowIfFailed(CreateDXGIFactory1(IID_PPV_ARGS(&amp;factory)));

    if (m_useWarpDevice)
    {
        ComPtr&lt;IDXGIAdapter&gt; warpAdapter;
        ThrowIfFailed(factory-&gt;EnumWarpAdapter(IID_PPV_ARGS(&amp;warpAdapter)));

        ThrowIfFailed(D3D12CreateDevice(
            warpAdapter.Get(),
            D3D_FEATURE_LEVEL_11_0,
            IID_PPV_ARGS(&amp;m_d3d12Device)
            ));
    }
    else
    {
        ComPtr&lt;IDXGIAdapter1&gt; hardwareAdapter;
        GetHardwareAdapter(factory.Get(), &amp;hardwareAdapter);

        ThrowIfFailed(D3D12CreateDevice(
            hardwareAdapter.Get(),
            D3D_FEATURE_LEVEL_11_0,
            IID_PPV_ARGS(&amp;m_d3d12Device)
            ));
    }

    // Describe and create the command queue.
    D3D12_COMMAND_QUEUE_DESC queueDesc = {};
    queueDesc.Flags = D3D12_COMMAND_QUEUE_FLAG_NONE;
    queueDesc.Type = D3D12_COMMAND_LIST_TYPE_DIRECT;

    ThrowIfFailed(m_d3d12Device-&gt;CreateCommandQueue(&amp;queueDesc, IID_PPV_ARGS(&amp;m_commandQueue)));

    // Describe the swap chain.
    DXGI_SWAP_CHAIN_DESC swapChainDesc = {};
    swapChainDesc.BufferCount = FrameCount;
    swapChainDesc.BufferDesc.Width = m_width;
    swapChainDesc.BufferDesc.Height = m_height;
    swapChainDesc.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
    swapChainDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
    swapChainDesc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_DISCARD;
    swapChainDesc.OutputWindow = Win32Application::GetHwnd();
    swapChainDesc.SampleDesc.Count = 1;
    swapChainDesc.Windowed = TRUE;

    ComPtr&lt;IDXGISwapChain&gt; swapChain;
    ThrowIfFailed(factory-&gt;CreateSwapChain(
        m_commandQueue.Get(),        // Swap chain needs the queue so that it can force a flush on it.
        &amp;swapChainDesc,
        &amp;swapChain
        ));

    ThrowIfFailed(swapChain.As(&amp;m_swapChain));

    // This sample does not support fullscreen transitions.
    ThrowIfFailed(factory-&gt;MakeWindowAssociation(Win32Application::GetHwnd(), DXGI_MWA_NO_ALT_ENTER));

    m_frameIndex = m_swapChain-&gt;GetCurrentBackBufferIndex();

    // Create an 11 device wrapped around the 12 device and share
    // 12's command queue.
    ComPtr&lt;ID3D11Device&gt; d3d11Device;
    ThrowIfFailed(D3D11On12CreateDevice(
        m_d3d12Device.Get(),
        d3d11DeviceFlags,
        nullptr,
        0,
        reinterpret_cast&lt;IUnknown**&gt;(m_commandQueue.GetAddressOf()),
        1,
        0,
        &amp;d3d11Device,
        &amp;m_d3d11DeviceContext,
        nullptr
        ));

    // Query the 11On12 device from the 11 device.
    ThrowIfFailed(d3d11Device.As(&amp;m_d3d11On12Device));

    // Create D2D/DWrite components.
    {
        D2D1_DEVICE_CONTEXT_OPTIONS deviceOptions = D2D1_DEVICE_CONTEXT_OPTIONS_NONE;
        ThrowIfFailed(D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, __uuidof(ID2D1Factory3), &amp;d2dFactoryOptions, &amp;m_d2dFactory));
        ComPtr&lt;IDXGIDevice&gt; dxgiDevice;
        ThrowIfFailed(m_d3d11On12Device.As(&amp;dxgiDevice));
        ThrowIfFailed(m_d2dFactory-&gt;CreateDevice(dxgiDevice.Get(), &amp;m_d2dDevice));
        ThrowIfFailed(m_d2dDevice-&gt;CreateDeviceContext(deviceOptions, &amp;m_d2dDeviceContext));
        ThrowIfFailed(DWriteCreateFactory(DWRITE_FACTORY_TYPE_SHARED, __uuidof(IDWriteFactory), &amp;m_dWriteFactory));
    }

    // Query the desktop's dpi settings, which will be used to create
    // D2D's render targets.
    float dpiX;
    float dpiY;
    m_d2dFactory-&gt;GetDesktopDpi(&amp;dpiX, &amp;dpiY);
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = D2D1::BitmapProperties1(
        D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
        D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX,
        dpiY
        );

    // Create descriptor heaps.
    {
        // Describe and create a render target view (RTV) descriptor heap.
        D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
        rtvHeapDesc.NumDescriptors = FrameCount;
        rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
        rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
        ThrowIfFailed(m_d3d12Device-&gt;CreateDescriptorHeap(&amp;rtvHeapDesc, IID_PPV_ARGS(&amp;m_rtvHeap)));

        m_rtvDescriptorSize = m_d3d12Device-&gt;GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
    }

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap-&gt;GetCPUDescriptorHandleForHeapStart());

        // Create a RTV, D2D render target, and a command allocator for each frame.
        for (UINT n = 0; n &lt; FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain-&gt;GetBuffer(n, IID_PPV_ARGS(&amp;m_renderTargets[n])));
            m_d3d12Device-&gt;CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);

            // Create a wrapped 11On12 resource of this back buffer. Since we are 
            // rendering all D3D12 content first and then all D2D content, we specify 
            // the In resource state as RENDER_TARGET - because D3D12 will have last 
            // used it in this state - and the Out resource state as PRESENT. When 
            // ReleaseWrappedResources() is called on the 11On12 device, the resource 
            // will be transitioned to the PRESENT state.
            D3D11_RESOURCE_FLAGS d3d11Flags = { D3D11_BIND_RENDER_TARGET };
            ThrowIfFailed(m_d3d11On12Device-&gt;CreateWrappedResource(
                m_renderTargets[n].Get(),
                &amp;d3d11Flags,
                D3D12_RESOURCE_STATE_RENDER_TARGET,
                D3D12_RESOURCE_STATE_PRESENT,
                IID_PPV_ARGS(&amp;m_wrappedBackBuffers[n])
                ));

            // Create a render target for D2D to draw directly to this back buffer.
            ComPtr&lt;IDXGISurface&gt; surface;
            ThrowIfFailed(m_wrappedBackBuffers[n].As(&amp;surface));
            ThrowIfFailed(m_d2dDeviceContext-&gt;CreateBitmapFromDxgiSurface(
                surface.Get(),
                &amp;bitmapProperties,
                &amp;m_d2dRenderTargets[n]
                ));

            rtvHandle.Offset(1, m_rtvDescriptorSize);

            ThrowIfFailed(m_d3d12Device-&gt;CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&amp;m_commandAllocators[n])));
        }
    
    }
}
</pre>
</td>
</tr>
</table></span></div>
Refer to the <a href="https://msdn.microsoft.com/en-us/library/Dn933255(v=VS.85).aspx">Example Code in the D3D12 Reference</a>.
          

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn913196(v=VS.85).aspx">11on12 Functions</a>
 

 

