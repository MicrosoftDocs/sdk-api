---
UID: NF:dcomp.IDCompositionDevice.CreateTargetForHwnd
title: IDCompositionDevice::CreateTargetForHwnd (dcomp.h)
description: Creates a composition target object that is bound to the window that is represented by the specified window handle (HWND).
helpviewer_keywords: ["CreateTargetForHwnd","CreateTargetForHwnd method [DirectComposition]","CreateTargetForHwnd method [DirectComposition]","IDCompositionDevice interface","IDCompositionDevice interface [DirectComposition]","CreateTargetForHwnd method","IDCompositionDevice.CreateTargetForHwnd","IDCompositionDevice::CreateTargetForHwnd","dcomp/IDCompositionDevice::CreateTargetForHwnd","directcomp.idcompositiondevice_createhwndtarget"]
old-location: directcomp\idcompositiondevice_createhwndtarget.htm
tech.root: directcomp
ms.assetid: eba2388a-9c94-43f0-bf7f-e814895a2792
ms.date: 12/05/2018
ms.keywords: CreateTargetForHwnd, CreateTargetForHwnd method [DirectComposition], CreateTargetForHwnd method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateTargetForHwnd method, IDCompositionDevice.CreateTargetForHwnd, IDCompositionDevice::CreateTargetForHwnd, dcomp/IDCompositionDevice::CreateTargetForHwnd, directcomp.idcompositiondevice_createhwndtarget
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionDevice::CreateTargetForHwnd
 - dcomp/IDCompositionDevice::CreateTargetForHwnd
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionDevice.CreateTargetForHwnd
---

# IDCompositionDevice::CreateTargetForHwnd


## -description

Creates a composition target object that is bound to the window that is represented by the specified window handle (<a href="/windows/desktop/WinProg/windows-data-types">HWND</a>).

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The window to which the  composition target object should be bound. This parameter must not be NULL.

### -param topmost [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

TRUE if the visual tree should be displayed on top of the children of the window specified by the <i>hwnd</i> parameter; otherwise, the visual tree is displayed behind the children.

### -param target [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontarget">IDCompositionTarget</a>**</b>

The new composition target object. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

A Microsoft DirectComposition visual tree must be bound to a window before anything can be displayed on screen. The window can be a top-level window or a child window. In either case, the window can be a layered window, but in all cases the window must belong to the calling process. If the window belongs to a different process, this method returns <a href="/windows/desktop/directcomp/directcomposition-error-codes">DCOMPOSITION_ERROR_ACCESS_DENIED</a>. 

When DirectComposition content is composed to the window, the content is always composed on top of whatever is drawn directly to that window through the device context (<a href="/windows/desktop/WinProg/windows-data-types">HDC</a>) returned by the <a href="/windows/desktop/api/winuser/nf-winuser-getdc">GetDC</a> function, or by calls to Microsoft DirectX <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">Present</a> methods. However, because window clipping rules apply to DirectComposition content, if the window has child windows, those child windows may clip the visual tree. The <i>topmost</i> parameter determines whether child windows clip the visual tree. 

 Conceptually, each window consists of four layers:

<ol>
<li>The contents drawn directly to the window handle (this is the bottommost layer).</li>
<li>An optional DirectComposition visual tree.</li>
<li>The contents of all child windows, if any.</li>
<li>Another optional DirectComposition visual tree (this is the topmost layer).</li>
</ol>
All four layers are clipped to the window's visible region.

At most, only two composition targets can be created for each window in the system, one topmost and one not topmost. If a composition target is already bound to the specified window at the specified layer, this method fails. When a composition target object is destroyed, the layer it composed is available for use by a new composition target object.


#### Examples

The following example creates and initializes a device object, and then binds the device object to a composition target window.


```cpp
#include <dcomp.h>
#include <d3d11.h>

HRESULT InitializeDirectCompositionDevice(HWND hwndTarget, 
        ID3D11Device **ppD3D11Device, IDCompositionDevice **ppDevice,
        IDCompositionTarget **ppCompTarget)
{
    HRESULT hr = S_OK;
    D3D_FEATURE_LEVEL featureLevelSupported;
    IDXGIDevice *pDXGIDevice = nullptr;

    // Verify that the arguments are valid.
    if (hwndTarget == NULL || ppD3D11Device == nullptr || ppDevice == nullptr || 
                            ppCompTarget == nullptr)
    {
        return E_INVALIDARG;
    }

    // Create the D3D device object. Note that the 
    // D3D11_CREATE_DEVICE_BGRA_SUPPORT flag is needed for rendering 
    // on surfaces using Direct2D. 
    hr = D3D11CreateDevice(
        nullptr,
        D3D_DRIVER_TYPE_HARDWARE,
        NULL,
        D3D11_CREATE_DEVICE_BGRA_SUPPORT, // needed for rendering on surfaces using Direct2D
        NULL,
        0,
        D3D11_SDK_VERSION,
        ppD3D11Device,
        &featureLevelSupported,
        NULL);

    if (SUCCEEDED(hr))
    {
        // Create the DXGI device used to create bitmap surfaces.
        hr = (*ppD3D11Device)->QueryInterface(&pDXGIDevice);
    }

    if (SUCCEEDED(hr))
    {
        // Create the DirectComposition device object.
        hr = DCompositionCreateDevice(pDXGIDevice, __uuidof(IDCompositionDevice), 
                reinterpret_cast<void **>(ppDevice));
    }

    if (SUCCEEDED(hr))
    {
        // Bind the DirectComposition device to the target window.
        hr = (*ppDevice)->CreateTargetForHwnd(hwndTarget, TRUE, ppCompTarget);   
    }

    return hr;
}

```

## -see-also

<a href="/windows/desktop/directcomp/basic-concepts">Composition Target Window</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontarget">IDCompositionTarget</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiontarget-setroot">IDCompositionTarget::SetRoot</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a>