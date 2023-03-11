---
UID: NF:d3d11on12.D3D11On12CreateDevice
title: D3D11On12CreateDevice function (d3d11on12.h)
description: Creates a device that uses Direct3D 11 functionality in Direct3D 12, specifying a pre-existing Direct3D 12 device to use for Direct3D 11 interop.
helpviewer_keywords: ["D3D11On12CreateDevice","D3D11On12CreateDevice function","d3d11on12/D3D11On12CreateDevice","direct3d12.d3d11on12createdevice"]
old-location: direct3d12\d3d11on12createdevice.htm
tech.root: direct3d12
ms.assetid: 6FC2CB44-4AA8-4E89-9E9B-ED1C3C9C64CC
ms.date: 12/05/2018
ms.keywords: D3D11On12CreateDevice, D3D11On12CreateDevice function, d3d11on12/D3D11On12CreateDevice, direct3d12.d3d11on12createdevice
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11On12CreateDevice
 - d3d11on12/D3D11On12CreateDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D11.dll
api_name:
 - D3D11On12CreateDevice
---

## -description

Creates a device that uses Direct3D 11 functionality in Direct3D 12, specifying a pre-existing Direct3D 12 device to use for Direct3D 11 interop.

## -parameters

### -param pDevice [in]

Type: <b>IUnknown*</b>

Specifies a pre-existing Direct3D 12 device to use for Direct3D 11 interop. May not be NULL.

### -param Flags

Type: <b>UINT</b>

One or more bitwise OR'd flags from <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag">D3D11_CREATE_DEVICE_FLAG</a>. These are the same flags as those used by <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain">D3D11CreateDeviceAndSwapChain</a>. Specifies which runtime <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">layers</a> to enable. <i>Flags</i> must be compatible with device flags, and its <i>NodeMask</i> must be a subset of the <i>NodeMask</i> provided to the present API.

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

The first feature level that is less than or equal to the Direct3D 12 device's feature level will be used to perform Direct3D 11 validation. Creation will fail if no acceptable feature levels are provided. Providing NULL will default to the Direct3D 12 device's feature level.

### -param FeatureLevels

Type: <b>UINT</b>

The size of (that is, the number of elements in) the *pFeatureLevels* array.

### -param ppCommandQueues [in, optional]

Type: <b>IUnknown* const *</b>

An array of unique queues for D3D11On12 to use. The queues must be of the 3D command queue type.

### -param NumQueues

Type: <b>UINT</b>

The size of (that is, the number of elements in) the *ppCommandQueues* array.

### -param NodeMask

Type: <b>UINT</b>

Which node of the Direct3D 12 device to use. Only 1 bit may be set.

### -param ppDevice [out, optional]

Type: <b>ID3D11Device**</b>

Pointer to the returned <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>. May be NULL.

### -param ppImmediateContext [out, optional]

Type: <b>ID3D11DeviceContext**</b>

A pointer to the returned <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>. May be NULL.

### -param pChosenFeatureLevel [out, optional]

Type: <b>D3D_FEATURE_LEVEL*</b>

A pointer to the returned feature level. May be NULL.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a> that are documented for <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice">D3D11CreateDevice</a>.          

This method returns <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_SDK_COMPONENT_MISSING</a> if you specify <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag">D3D11_CREATE_DEVICE_DEBUG</a> in <i>Flags</i> and the incorrect version of the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">debug layer</a> is installed on your computer. Install the latest Windows SDK to get the correct version.

## -remarks

The function signature PFN_D3D11ON12_CREATE_DEVICE is provided as a typedef, so that you can use dynamic linking techniques (<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>) instead of statically linking.

## Examples

To render text over Direct3D 12 using Direct2D via the 11On12 device, load the rendering pipeline dependencies.

```cpp
// Load the rendering pipeline dependencies.
void D3D1211on12::LoadPipeline()
{
    UINT d3d11DeviceFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
    D2D1_FACTORY_OPTIONS d2dFactoryOptions = {};
#if defined(_DEBUG)
    // Enable the D2D debug layer.
    d2dFactoryOptions.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;

    // Enable the Direct3D 11 debug layer.
    d3d11DeviceFlags |= D3D11_CREATE_DEVICE_DEBUG;
    
    // Enable the Direct3D 12 debug layer.
    {
        ComPtr<ID3D12Debug> debugController;
        if (SUCCEEDED(D3D12GetDebugInterface(IID_PPV_ARGS(&debugController))))
        {
            debugController->EnableDebugLayer();
        }
    }
#endif

    ComPtr<IDXGIFactory4> factory;
    ThrowIfFailed(CreateDXGIFactory1(IID_PPV_ARGS(&factory)));

    if (m_useWarpDevice)
    {
        ComPtr<IDXGIAdapter> warpAdapter;
        ThrowIfFailed(factory->EnumWarpAdapter(IID_PPV_ARGS(&warpAdapter)));

        ThrowIfFailed(D3D12CreateDevice(
            warpAdapter.Get(),
            D3D_FEATURE_LEVEL_11_0,
            IID_PPV_ARGS(&m_d3d12Device)
            ));
    }
    else
    {
        ComPtr<IDXGIAdapter1> hardwareAdapter;
        GetHardwareAdapter(factory.Get(), &hardwareAdapter);

        ThrowIfFailed(D3D12CreateDevice(
            hardwareAdapter.Get(),
            D3D_FEATURE_LEVEL_11_0,
            IID_PPV_ARGS(&m_d3d12Device)
            ));
    }

    // Describe and create the command queue.
    D3D12_COMMAND_QUEUE_DESC queueDesc = {};
    queueDesc.Flags = D3D12_COMMAND_QUEUE_FLAG_NONE;
    queueDesc.Type = D3D12_COMMAND_LIST_TYPE_DIRECT;

    ThrowIfFailed(m_d3d12Device->CreateCommandQueue(&queueDesc, IID_PPV_ARGS(&m_commandQueue)));

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

    ComPtr<IDXGISwapChain> swapChain;
    ThrowIfFailed(factory->CreateSwapChain(
        m_commandQueue.Get(),        // Swap chain needs the queue so that it can force a flush on it.
        &swapChainDesc,
        &swapChain
        ));

    ThrowIfFailed(swapChain.As(&m_swapChain));

    // This sample does not support fullscreen transitions.
    ThrowIfFailed(factory->MakeWindowAssociation(Win32Application::GetHwnd(), DXGI_MWA_NO_ALT_ENTER));

    m_frameIndex = m_swapChain->GetCurrentBackBufferIndex();

    // Create an 11 device wrapped around the 12 device and share
    // 12's command queue.
    ComPtr<ID3D11Device> d3d11Device;
    ThrowIfFailed(D3D11On12CreateDevice(
        m_d3d12Device.Get(),
        d3d11DeviceFlags,
        nullptr,
        0,
        reinterpret_cast<IUnknown**>(m_commandQueue.GetAddressOf()),
        1,
        0,
        &d3d11Device,
        &m_d3d11DeviceContext,
        nullptr
        ));

    // Query the 11On12 device from the 11 device.
    ThrowIfFailed(d3d11Device.As(&m_d3d11On12Device));

    // Create D2D/DWrite components.
    {
        D2D1_DEVICE_CONTEXT_OPTIONS deviceOptions = D2D1_DEVICE_CONTEXT_OPTIONS_NONE;
        ThrowIfFailed(D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            __uuidof(ID2D1Factory3),
            &d2dFactoryOptions,
            &m_d2dFactory));
        ComPtr<IDXGIDevice> dxgiDevice;
        ThrowIfFailed(m_d3d11On12Device.As(&dxgiDevice));
        ThrowIfFailed(m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice));
        ThrowIfFailed(m_d2dDevice->CreateDeviceContext(deviceOptions, &m_d2dDeviceContext));
        ThrowIfFailed(DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            &m_dWriteFactory));
    }

    // Query the desktop's dpi settings, which will be used to create
    // D2D's render targets.
    float dpi = GetDpiForWindow(Win32Application::GetHwnd());
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = D2D1::BitmapProperties1(
        D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
        D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpi,
        dpi
        );

    // Create descriptor heaps.
    {
        // Describe and create a render target view (RTV) descriptor heap.
        D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
        rtvHeapDesc.NumDescriptors = FrameCount;
        rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
        rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
        ThrowIfFailed(m_d3d12Device->CreateDescriptorHeap(&rtvHeapDesc, IID_PPV_ARGS(&m_rtvHeap)));

        m_rtvDescriptorSize = 
            m_d3d12Device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
    }

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV, D2D render target, and a command allocator for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_d3d12Device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);

            // Create a wrapped 11On12 resource of this back buffer. Since we are 
            // rendering all Direct3D 12 content first and then all D2D content, we specify 
            // the In resource state as RENDER_TARGET - because Direct3D 12 will have last 
            // used it in this state - and the Out resource state as PRESENT. When 
            // ReleaseWrappedResources() is called on the 11On12 device, the resource 
            // will be transitioned to the PRESENT state.
            D3D11_RESOURCE_FLAGS d3d11Flags = { D3D11_BIND_RENDER_TARGET };
            ThrowIfFailed(m_d3d11On12Device->CreateWrappedResource(
                m_renderTargets[n].Get(),
                &d3d11Flags,
                D3D12_RESOURCE_STATE_RENDER_TARGET,
                D3D12_RESOURCE_STATE_PRESENT,
                IID_PPV_ARGS(&m_wrappedBackBuffers[n])
                ));

            // Create a render target for D2D to draw directly to this back buffer.
            ComPtr<IDXGISurface> surface;
            ThrowIfFailed(m_wrappedBackBuffers[n].As(&surface));
            ThrowIfFailed(m_d2dDeviceContext->CreateBitmapFromDxgiSurface(
                surface.Get(),
                &bitmapProperties,
                &m_d2dRenderTargets[n]
                ));

            rtvHandle.Offset(1, m_rtvDescriptorSize);

            ThrowIfFailed(m_d3d12Device->CreateCommandAllocator(
                D3D12_COMMAND_LIST_TYPE_DIRECT,
                IID_PPV_ARGS(&m_commandAllocators[n])));
        }
    }
}
```

See the notes about the [Example code in the Direct3D 12 reference content](/windows/win32/direct3d12/notes-on-example-code).

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-11-on-12-functions-">11on12 Functions</a>
