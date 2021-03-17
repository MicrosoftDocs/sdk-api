---
UID: NF:holographicspaceinterop.IHolographicSpaceInterop.CreateForWindow
title: IHolographicSpaceInterop::CreateForWindow (holographicspaceinterop.h)
description: Instantiates a HolographicSpace object and binds it to the current application.
helpviewer_keywords: ["CreateForWindow","CreateForWindow method","CreateForWindow method","IHolographicSpaceInterop interface","IHolographicSpaceInterop interface","CreateForWindow method","IHolographicSpaceInterop.CreateForWindow","IHolographicSpaceInterop::CreateForWindow","MixedReality.iholographicspaceinterop_createforwindow","holographicspaceinterop/IHolographicSpaceInterop::CreateForWindow"]
old-location: mixedreality\iholographicspaceinterop_createforwindow.htm
tech.root: MixedReality
ms.assetid: 8B7A226E-FB47-4BA2-B13E-B37250C75920
ms.date: 01/25/2019
ms.keywords: CreateForWindow, CreateForWindow method, CreateForWindow method,IHolographicSpaceInterop interface, IHolographicSpaceInterop interface,CreateForWindow method, IHolographicSpaceInterop.CreateForWindow, IHolographicSpaceInterop::CreateForWindow, MixedReality.iholographicspaceinterop_createforwindow, holographicspaceinterop/IHolographicSpaceInterop::CreateForWindow
req.header: holographicspaceinterop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: HolographicSpaceInterop.idl
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
f1_keywords:
 - IHolographicSpaceInterop::CreateForWindow
 - holographicspaceinterop/IHolographicSpaceInterop::CreateForWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - HolographicSpaceInterop.h
api_name:
 - IHolographicSpaceInterop.CreateForWindow
---

# IHolographicSpaceInterop::CreateForWindow


## -description

Instantiates a [HolographicSpace](/uwp/api/windows.graphics.holographic.holographicspace) object, and binds it to the current application.

## -parameters

### -param window [in]

Type: [HWND](/windows/desktop/winprog/windows-data-types)

Handle to the window of the active application.

### -param riid [in]

Type: **REFIID**

The RUID for the resource interface.

The REFIID, or GUID, of the interface to the resource can be obtained by using the __uuidof() macro. For example, __uuidof(IRadialController) will get the GUID of the interface to a buffer resource.

### -param holographicSpace [out]

Type: **void\*\***

Address of a pointer to a [HolographicSpace](/uwp/api/windows.graphics.holographic.holographicspace) object.

## -returns

Type: **HRESULT**

If this function succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

This example shows how to use **IHolographicSpaceInterop::CreateForWindow** to create and use a [HolographicSpace](/uwp/api/windows.graphics.holographic.holographicspace) for an [HWND](/windows/desktop/winprog/windows-data-types). See the [basic hologram sample](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/BasicHologram) for more info.


```cppwinrt
// This code example depends on these headers.
// <HolographicSpaceInterop.h>
// <Windows.Graphics.Holographic.h>
// <winrt/Windows.Graphics.Holographic.h>

// Create the window for the HolographicSpace.
hWnd = CreateWindowW(
    m_szWindowClass, 
    m_szTitle,
    WS_VISIBLE,
    CW_USEDEFAULT, 
    0, 
    CW_USEDEFAULT, 
    0, 
    nullptr, 
    nullptr, 
    hInstance, 
    nullptr);
 
if (!hWnd)
{
    winrt::check_hresult(E_FAIL);
}
 
{
    // Use WinRT factory to create the holographic space.
    using namespace winrt::Windows::Graphics::Holographic;
    winrt::com_ptr<IHolographicSpaceInterop> holographicSpaceInterop = winrt::get_activation_factory<HolographicSpace, IHolographicSpaceInterop>();
    winrt::com_ptr<ABI::Windows::Graphics::Holographic::IHolographicSpace> spHolographicSpace;
    winrt::check_hresult(holographicSpaceInterop->CreateForWindow(hWnd, __uuidof(ABI::Windows::Graphics::Holographic::IHolographicSpace), winrt::put_abi(spHolographicSpace)));
 
    if (!spHolographicSpace)
    {
        winrt::check_hresult(E_FAIL);
    }
 
    // Store the holographic space.
    m_holographicSpace = spHolographicSpace.as<HolographicSpace>();
}
 
// The DeviceResources class uses the preferred DXGI adapter ID from the holographic
// space (when available) to create a Direct3D device. The HolographicSpace
// uses this ID3D11Device to create and manage device-based resources such as
// swap chains.
m_deviceResources->SetHolographicSpace(m_holographicSpace);
 
// The main class uses the holographic space for updates and rendering.
m_main->SetHolographicSpace(hWnd, m_holographicSpace);
 
// Show the window. This activates the holographic view, and switches focus to the app in Windows Mixed Reality.
ShowWindow(hWnd, nCmdShow);
UpdateWindow(hWnd);
```

## -see-also

* [IHolographicSpaceInterop](nn-holographicspaceinterop-iholographicspaceinterop.md)
* [HolographicSpace](/uwp/api/windows.graphics.holographic.holographicspace)
* [Mixed Reality Dev Center](/windows/mixed-reality)
* [Windows.Graphics.Holographic](/uwp/api/windows.graphics.holographic)

