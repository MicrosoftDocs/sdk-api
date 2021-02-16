---
UID: NF:spatialinteractionmanagerinterop.ISpatialInteractionManagerInterop.GetForWindow
title: ISpatialInteractionManagerInterop::GetForWindow (spatialinteractionmanagerinterop.h)
description: Retrieves a SpatialInteractionManager object bound to the active application.
helpviewer_keywords: ["GetForWindow","GetForWindow method","GetForWindow method","ISpatialInteractionManagerInterop interface","ISpatialInteractionManagerInterop interface","GetForWindow method","ISpatialInteractionManagerInterop.GetForWindow","ISpatialInteractionManagerInterop::GetForWindow","MixedReality.ispatialinteractionmanager_getforwindow","spatialinteractionmanagerinterop/ISpatialInteractionManagerInterop::GetForWindow"]
old-location: mixedreality\ispatialinteractionmanager_getforwindow.htm
tech.root: MixedReality
ms.assetid: 5D11BF4D-2EE3-40A3-A1EE-202DD5B904FE
ms.date: 01/25/2019
ms.keywords: GetForWindow, GetForWindow method, GetForWindow method,ISpatialInteractionManagerInterop interface, ISpatialInteractionManagerInterop interface,GetForWindow method, ISpatialInteractionManagerInterop.GetForWindow, ISpatialInteractionManagerInterop::GetForWindow, MixedReality.ispatialinteractionmanager_getforwindow, spatialinteractionmanagerinterop/ISpatialInteractionManagerInterop::GetForWindow
req.header: spatialinteractionmanagerinterop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SpatialInteractionManagerInterop.idl
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
 - ISpatialInteractionManagerInterop::GetForWindow
 - spatialinteractionmanagerinterop/ISpatialInteractionManagerInterop::GetForWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SpatialInteractionManagerInterop.h
api_name:
 - ISpatialInteractionManagerInterop.GetForWindow
---

# ISpatialInteractionManagerInterop::GetForWindow


## -description

Retrieves a [SpatialInteractionManager](/uwp/api/windows.ui.input.spatial.spatialinteractionmanager) object bound to the active application.

## -parameters

### -param window [in]

Type: [HWND](/windows/desktop/winprog/windows-data-types)

Handle to the window of the active application.

### -param riid [in]

Type: **REFIID**

The GUID of the [SpatialInteractionManager](/uwp/api/windows.ui.input.spatial.spatialinteractionmanager) object.

### -param spatialInteractionManager [out]

Type: **void\*\***

Address of a pointer to a [SpatialInteractionManager](/uwp/api/windows.ui.input.spatial.spatialinteractionmanager) object.

## -returns

Type: **HRESULT**

If this function succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

This example shows how to retrieve a [SpatialInteractionManager](/uwp/api/windows.ui.input.spatial.spatialinteractionmanager) by using **ISpatialInteractionManagerInterop::GetForWindow** to retrieve the **SpatialInteractionManager** for an [HWND](/windows/desktop/winprog/windows-data-types).

```cppwinrt
// This code example depends on these headers.
// <SpatialInteractionManagerInterop.h>
// <Windows.UI.Input.Spatial.h>
// <winrt/Windows.UI.Input.Spatial.h>
 
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
    using namespace winrt::Windows::UI::Input::Spatial;
    winrt::com_ptr<ISpatialInteractionManagerInterop> spatialInteractionManagerInterop = 
        winrt::get_activation_factory<SpatialInteractionManager, ISpatialInteractionManagerInterop>();
 
    winrt::com_ptr<ABI::Windows::UI::Input::Spatial::ISpatialInteractionManager> spSpatialInteractionManager;
    winrt::check_hresult(spatialInteractionManagerInterop->GetForWindow(hWnd, __uuidof(ABI::Windows::UI::Input::Spatial::ISpatialInteractionManager), winrt::put_abi(spSpatialInteractionManager)));
 
    SpatialInteractionManager spatialInteractionManager = spSpatialInteractionManager.as<SpatialInteractionManager>();
}
```

## -see-also

* [ISpatialInteractionManagerInterop](nn-spatialinteractionmanagerinterop-ispatialinteractionmanagerinterop.md)
* [SpatialInteractionManager](/uwp/api/windows.ui.input.spatial.spatialinteractionmanager)
* [Mixed Reality Dev Center](/windows/mixed-reality)
* [Windows.Graphics.Holographic](/uwp/api/windows.graphics.holographic)

