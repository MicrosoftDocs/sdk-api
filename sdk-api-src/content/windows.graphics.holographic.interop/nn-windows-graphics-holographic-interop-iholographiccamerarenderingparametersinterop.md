---
UID: NN:windows.graphics.holographic.interop.IHolographicCameraRenderingParametersInterop
title: IHolographicCameraRenderingParametersInterop
description: A nano-COM interface that allows COM interop with the [HolographicCameraRenderingParameters](/uwp/api/windows.graphics.holographic.holographiccamerarenderingparameters) class for applications that use Direct3D 12 for holographic rendering.
tech.root: direct3d12
ms.date: 12/12/2019
ms.topic: language-reference
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
 - interop::IHolographicCameraRenderingParametersInterop
 - IHolographicCameraRenderingParametersInterop
f1_keywords:
 - IHolographicCameraRenderingParametersInterop
 - windows.graphics.holographic.interop/IHolographicCameraRenderingParametersInterop
dev_langs:
 - c++
---

## -description

The **IHolographicCameraRenderingParametersInterop** interface is a nano-COM interface, used to commit Direct3D 12 buffer resources for presentation during the corresponding [HolographicFrame](/uwp/api/windows.graphics.holographic.holographicframe).

The interface allows COM interop with the [HolographicCameraRenderingParameters](/uwp/api/windows.graphics.holographic.holographiccamerarenderingparameters) Windows Runtime class for applications that use Direct3D 12 for holographic rendering. Nano-COM allows Direct3D 12 objects to be used directly as parameters for API calls, rather than going through a container object.

## -inheritance

The **IHolographicCameraRenderingParametersInterop** interface inherits from the [IInspectable](../inspectable/nn-inspectable-iinspectable.md) interface.

## -remarks

To use this interface in [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/), retrieve the [HolographicCameraRenderingParameters](/uwp/api/windows.graphics.holographic.holographiccamerarenderingparameters) object from the [HolographicFrame](/uwp/api/windows.graphics.holographic.holographicframe), and then **QueryInterface** for the **IHolographicCameraRenderingParametersInterop** interface.

```cppwinrt
auto holographicCameraRenderingParameters { holographicFrame.GetRenderingParameters(m_cameraPose) };
winrt::com_ptr<IHolographicCameraRenderingParametersInterop> holographicCameraRenderingParametersInterop
{
    holographicCameraRenderingParameters.as<IHolographicCameraRenderingParametersInterop>();
};
```

To use this interface in C++/CX, first cast the [HolographicCameraRenderingParameters](/uwp/api/windows.graphics.holographic.holographiccamerarenderingparameters) object (after retrieving it from the [HolographicFrame](/uwp/api/windows.graphics.holographic.holographicframe)) to [IInspectable](../inspectable/nn-inspectable-iinspectable.md)\*. Then **QueryInterface** for the **IHolographicCameraRenderingParametersInterop** interface from the **IInspectable** pointer.

```cppcx
auto holographicCameraRenderingParameters = 
    holographicFrame->GetRenderingParameters(m_cameraPose);
Microsoft::WRL::ComPtr<IHolographicCameraRenderingParametersInterop> 
    holographicCameraRenderingParametersInterop;
{
    Microsoft::WRL::ComPtr<IInspectable> iInspectable = reinterpret_cast<IInspectable*>(holographicCameraRenderingParameters);
    DX::ThrowIfFailed(iInspectable.As(&holographicCameraRenderingParametersInterop));
}
```

## -see-also