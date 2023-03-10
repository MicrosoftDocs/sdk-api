---
UID: NF:dcomp.DCompositionCreateDevice
title: DCompositionCreateDevice function (dcomp.h)
description: Creates a new device object that can be used to create other Microsoft DirectComposition objects. (DCompositionCreateDevice)
helpviewer_keywords: ["DCompositionCreateDevice","DCompositionCreateDevice function [DirectComposition]","dcomp/DCompositionCreateDevice","directcomp.dcompositioncreatedevice"]
old-location: directcomp\dcompositioncreatedevice.htm
tech.root: directcomp
ms.assetid: 3eb5d698-3cbf-456e-aa5f-395687c68c13
ms.date: 12/05/2018
ms.keywords: DCompositionCreateDevice, DCompositionCreateDevice function [DirectComposition], dcomp/DCompositionCreateDevice, directcomp.dcompositioncreatedevice
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
 - DCompositionCreateDevice
 - dcomp/DCompositionCreateDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dcomp.dll
api_name:
 - DCompositionCreateDevice
---

# DCompositionCreateDevice function


## -description

Creates a new device object that can be used to create other Microsoft DirectComposition objects.

## -parameters

### -param dxgiDevice [in]

Type: <b><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a>*</b>

The DXGI device to use to create DirectComposition surface objects.

### -param iid [in]

Type: <b>REFIID</b>

The identifier of the interface to retrieve.

### -param dcompositionDevice [out]

Type: <b>void**</b>

Receives an interface pointer to the newly created device object. The pointer is of the type specified by the <i>iid</i> parameter. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

A  device object serves as the factory for all other DirectComposition objects. It also controls transactional composition through the <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-commit">IDCompositionDevice::Commit</a> method.

The DXGI device specified by <i>dxgiDevice</i> is used to create all DirectComposition surface objects. In particular, the <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-begindraw">IDCompositionSurface::BeginDraw</a> method returns an interface pointer to a DXGI surface that belongs to the device specified by the <i>dxgiDevice</i> parameter.



When creating the DXGI device, developers must specify the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag">D3D11_CREATE_DEVICE BGRA_SUPPORT</a> or <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag">D3D10_CREATE_DEVICE_BGRA_SUPPORT</a> flag for Direct2D interoperability with Microsoft Direct3D resources.

The <i>iid</i> parameter must be <code>__uuidof(IDCompositionDevice)</code>, and the <i>dcompositionDevice</i> parameter receives a pointer to an <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a> interface.



#### Examples

The following example shows how to create a device object as part of initialing DirectComposition objects.


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

<a href="/windows/desktop/directcomp/functions">Functions</a>
