---
UID: NN:windows.graphics.holographic.interop.IHolographicCameraInterop
title: IHolographicCameraInterop
description: Extends [HolographicCamera](/uwp/api/windows.graphics.holographic.holographiccamera) to allow 2D texture resources to be created and used as back buffers for holographic rendering in Direct3D 12.
tech.root: direct3d12
ms.date: 12/12/2019
targetos: Windows
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: windows.graphics.holographic.interop.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - windows.graphics.holographic.interop.h
api_name:
 - interop::IHolographicCameraInterop
 - IHolographicCameraInterop
f1_keywords:
 - IHolographicCameraInterop
 - windows.graphics.holographic.interop/IHolographicCameraInterop
dev_langs:
 - c++
---

## -description

The **IHolographicCameraInterop** interface is a nano-COM interface, used to create Direct3D 12 back buffer resources for a [HolographicCamera](/uwp/api/windows.graphics.holographic.holographiccamera) Windows Runtime object. This is an initialization step for using Direct3D 12 with Windows Mixed Reality. This interface also allows your application to acquire ownership of content buffers for rendering, prior to committing them with the [HolographicCameraRenderingParametersInterop](./nn-windows-graphics-holographic-interop-iholographiccamerarenderingparametersinterop.md) interface.

Your application can use this interface to initialize holographic rendering using Direct3D 12. Nano-COM allows pointers to Direct3D 12 objects to be passed directly as parameters for API calls, instead of using a Windows Runtime container object.

Your application manages its own pool of holographic buffer resources for use as render targets (back buffers) for each [HolographicCamera](/uwp/api/windows.graphics.holographic.holographiccamera). It can create additional buffers as needed in order to continue rendering smoothly. On most devices, this will be three or four surfaces. Your application should start with at least two buffers in the pool. Your application can dynamically detect when it needs to create a new buffer by looking for unsuccessful attempts to immediately acquire buffers that were previously committed for presentation. Your application must commit a buffer for a **HolographicCamera** that is included on the [HolographicFrame](/uwp/api/windows.graphics.holographic.holographicframe) unless the primary layer is disabled for that camera, in which case your application must not commit a buffer for that camera.

A buffer created by a [HolographicCamera](/uwp/api/windows.graphics.holographic.holographiccamera) object can be used only with that object. It should be released when the **HolographicCamera** is released, or when the Direct3D 12 device needs to be recreated&mdash;whichever happens first. The buffer must not be in the GPU pipeline when it is released&mdash;Direct3D 12 fences should be used to ensure that this condition is met prior to releasing the buffer object.

## -inheritance

The **IHolographicCameraInterop** interface inherits from the [IInspectable](../inspectable/nn-inspectable-iinspectable.md) interface.

## -remarks

To use this interface in [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/), **QueryInterface** for the **IHolographicCameraInterop** interface from the [HolographicCamera](/uwp/api/windows.graphics.holographic.holographiccamera) object.

```cppwinrt
winrt::com_ptr<IHolographicCameraInterop> spCameraInterop {
    m_holographicCamera.as<IHolographicCameraInterop>() };

D3D12_RESOURCE_DESC bufferDesc { };
bufferDesc.Format =
  SelectFormatUsingHolographicViewConfiguration(
    m_holographicCamera.ViewConfiguration());
bufferDesc.SampleDesc.Count = 1;
bufferDesc.SampleDesc.Quality = 0;
bufferDesc.MipLevels = 1;
bufferDesc.Width = static_cast<UINT64>(
  m_holographicCamera.ViewConfiguration().RenderTargetSize().Width);
bufferDesc.Height = static_cast<UINT64>(
  m_holographicCamera.ViewConfiguration().RenderTargetSize().Height);

winrt::check_hresult(
  spCameraInterop->CreateDirect3D12BackBufferResource(
    m_deviceResources->GetD3D12Device(),
    &bufferDesc,
    &m_D3D12BackBuffer[m_contentBufferIndex]));
```

You can use the [HolographicViewConfiguration](/uwp/api/windows.graphics.holographic.holographicviewconfiguration) API to determine the available options for buffer format, and to acquire information about render target size for the corresponding output&mdash;for example, the [HolographicDisplay](/uwp/api/windows.graphics.holographic.holographicdisplay). If your application needs to change the buffer size for Direct3D 12 buffers from the default render target size for the [HolographicCamera](/uwp/api/windows.graphics.holographic.holographiccamera), then it should either request a new render target size using the [HolographicViewConfiguration::RequestRenderTargetSize](/uwp/api/windows.graphics.holographic.holographicviewconfiguration.requestrendertargetsize) method and create buffers using the size returned by that method, or choose an arbitrary size and override the viewport as described in the following paragraph.

Your Direct3D 12 application can use a viewport size chosen independently by the application. In that case, you must call the [HolographicCameraPose.OverrideViewport](/uwp/api/windows.graphics.holographic.holographiccamerapose.overrideviewport) method each frame to inform the platform about the viewport used for rendering.

The following code excerpt is from the [Windows Mixed Reality Direct3D 12 app template](https://marketplace.visualstudio.com/items?itemName=WindowsMixedRealityteam.WindowsMixedRealityAppTemplatesVSIX), which includes boilerplate code for most APIs that are provided in the `Windows.Graphics.Holographic.Interop.h` header.

```cppwinrt
winrt::com_ptr<IHolographicCameraInterop> spCameraInterop = 
    m_holographicCamera.as<IHolographicCameraInterop>();
winrt::check_hresult(
    spCameraInterop->CreateDirect3D12BackBufferResource(
        spD3D12Device.get(),
        &bufferDesc,
        m_spD3D12BackBuffer[bufferSlot].put()));
```

## -see-also