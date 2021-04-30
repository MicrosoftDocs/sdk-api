---
UID: NN:windows.graphics.holographic.interop.IHolographicQuadLayerUpdateParametersInterop
title: IHolographicQuadLayerUpdateParametersInterop
description: A nano-COM interface that allows COM interop with the [HolographicQuadLayerUpdateParameters](/uwp/api/windows.graphics.holographic.holographicquadlayerupdateparameters) class for applications that use Direct3D 12 for holographic rendering.
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
 - interop::IHolographicQuadLayerUpdateParametersInterop
 - IHolographicQuadLayerUpdateParametersInterop
f1_keywords:
 - IHolographicQuadLayerUpdateParametersInterop
 - windows.graphics.holographic.interop/IHolographicQuadLayerUpdateParametersInterop
dev_langs:
 - c++
---

## -description

The **IHolographicQuadLayerUpdateParametersInterop** interface is a nano-COM interface, used to commit Direct3D 12 buffer resources for quad layer rendering in the corresponding [HolographicFrame](/uwp/api/windows.graphics.holographic.holographicframe).

The interface allows COM interop with the [HolographicQuadLayerUpdateParameters](/uwp/api/windows.graphics.holographic.holographicquadlayerupdateparameters) class for applications that use Direct3D 12 for holographic rendering. Nano-COM allows Direct3D 12 objects to be used directly as parameters for API calls, rather than going through a container object.

## -inheritance

The **IHolographicQuadLayerUpdateParametersInterop** interface inherits from the [IInspectable](../inspectable/nn-inspectable-iinspectable.md) interface.

## -remarks

To use this interface in [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/), retrieve the [HolographicQuadLayerUpdateParameters](/uwp/api/windows.graphics.holographic.holographicquadlayerupdateparameters) object from the [HolographicFrame](/uwp/api/windows.graphics.holographic.holographicframe), and then QueryInterface for the **IHolographicQuadLayerUpdateParametersInterop** interface.

```cppwinrt
auto quadLayerParameters{ holographicFrame.GetQuadLayerUpdateParameters(m_quadLayer) };
winrt::com_ptr<IHolographicQuadLayerUpdateParametersInterop> quadLayerParametersInterop{
    quadLayerParameters.as<IHolographicQuadLayerUpdateParametersInterop>() };
```

To use this interface in C++/CX, first cast the [HolographicQuadLayerUpdateParameters](/uwp/api/windows.graphics.holographic.holographicquadlayerupdateparameters) object (after retrieving it from the [HolographicFrame](/uwp/api/windows.graphics.holographic.holographicframe)) to [IInspectable](../inspectable/nn-inspectable-iinspectable.md)\*. Then QueryInterface for the **IHolographicQuadLayerUpdateParametersInterop** interface from the **IInspectable** pointer.

```cppcx
auto quadLayerParameters = holographicFrame->GetQuadLayerUpdateParameters(m_quadLayer);
Microsoft::WRL::ComPtr<IHolographicQuadLayerUpdateParametersInterop> quadLayerParametersInterop;
{
    Microsoft::WRL::ComPtr<IInspectable> iInspectable = reinterpret_cast<IInspectable*>(quadLayerParameters);
    DX::ThrowIfFailed(iInspectable.As(&quadLayerParamsInterop));
}
```

## -see-also