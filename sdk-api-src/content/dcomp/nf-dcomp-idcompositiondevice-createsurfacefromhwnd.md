---
UID: NF:dcomp.IDCompositionDevice.CreateSurfaceFromHwnd
title: IDCompositionDevice::CreateSurfaceFromHwnd (dcomp.h)
description: The IDCompositionDevice::CreateSurfaceFromHwnd method creates a wrapper object that represents the rasterization of a layered window, and that can be associated with a visual for composition.
helpviewer_keywords: ["CreateSurfaceFromHwnd","CreateSurfaceFromHwnd method [DirectComposition]","CreateSurfaceFromHwnd method [DirectComposition]","IDCompositionDevice interface","IDCompositionDevice interface [DirectComposition]","CreateSurfaceFromHwnd method","IDCompositionDevice.CreateSurfaceFromHwnd","IDCompositionDevice::CreateSurfaceFromHwnd","dcomp/IDCompositionDevice::CreateSurfaceFromHwnd","directcomp.idcompositiondevice_createsurfacefromhwnd"]
old-location: directcomp\idcompositiondevice_createsurfacefromhwnd.htm
tech.root: directcomp
ms.assetid: EA49F8EB-FAC8-421E-854D-C4AA81887EB0
ms.date: 06/23/2022
ms.keywords: CreateSurfaceFromHwnd, CreateSurfaceFromHwnd method [DirectComposition], CreateSurfaceFromHwnd method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateSurfaceFromHwnd method, IDCompositionDevice.CreateSurfaceFromHwnd, IDCompositionDevice::CreateSurfaceFromHwnd, dcomp/IDCompositionDevice::CreateSurfaceFromHwnd, directcomp.idcompositiondevice_createsurfacefromhwnd
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
 - IDCompositionDevice::CreateSurfaceFromHwnd
 - dcomp/IDCompositionDevice::CreateSurfaceFromHwnd
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
 - IDCompositionDevice.CreateSurfaceFromHwnd
---

## -description

Creates a wrapper object that represents the rasterization of a layered window, and that can be associated with a visual for composition.

## -parameters

### -param hwnd

Type: [in] <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The handle of the layered window for which to create a  wrapper. A layered window is created by specifying <b>WS_EX_LAYERED</b> when creating the window with the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a> function or by setting <b>WS_EX_LAYERED</b> via <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga">SetWindowLong</a> after the window has been created.

### -param surface

Type: [out] <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

The new composition surface object. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

You can use the <i>surface</i> pointer in calls to the <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-setcontent">IDCompositionVisual::SetContent</a> method to set the content of one or more visuals. After setting the content, the visuals compose the contents of the specified layered window as long as the window is layered. If the window is unlayered, the window content disappears from the output of the composition tree. If the window is later re-layered, the window content reappears as long as it is still associated with a visual.

If the window is resized, the affected visuals are re-composed. 

The contents of the window are not cached beyond the life of the window. That is, if the window is destroyed, the affected visuals stop composing the window.

If the window is moved off-screen or resized to zero, the system stops composing the content of visuals. You should use the <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute">DwmSetWindowAttribute</a> function with the <b>DWMWA_CLOAK</b> flag to "cloak" the layered child window when you need to hide the original window while allowing the system to continue to compose the content of the visuals. For more information, see <a href="/windows/desktop/directcomp/how-to--animate-the-bitmap-of-a-layered-child-window">How to animate the bitmap of a layered child window</a> and <a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionLayeredChildWindow">DirectComposition layered child window sample</a>.

## Examples

The following code snippet creates a wrapper object that represents the rasterization of a layered window.

```cpp
HRESULT hr = S_OK;
IDCompositionVisual *pVisual = nullptr;
IUnknown *pSurface = nullptr;

// Create a visual. g_pDevice is the IDCompositionDevice pointer of a 
// device object created earlier.
hr = g_pDevice->CreateVisual(&pVisual);

if (SUCCEEDED(hr))
{
    // Create a surface that contains the image of the layered child 
    // window identified by the g_hwndChild window handle (HWND). 
    hr = g_pDevice->CreateSurfaceFromHwnd(g_hwndChild, &pSurface);
}

if (SUCCEEDED(hr))
{
    // Set the content of the Control child visual.
    hr = pVisual->SetContent(pSurface);
}
```

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a>

<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-createsurface">IDCompositionDevice::CreateSurface</a>

<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-createsurfacefromhandle">IDCompositionDevice::CreateSurfaceFromHandle</a>