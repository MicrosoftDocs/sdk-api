---
UID: NF:dcomp.IDCompositionDevice.CreateVirtualSurface
title: IDCompositionDevice::CreateVirtualSurface (dcomp.h)
description: The IDCompositionDevice::CreateVirtualSurface method creates a sparsely populated surface that can be associated with one or more visuals for composition.
helpviewer_keywords: ["CreateVirtualSurface","CreateVirtualSurface method [DirectComposition]","CreateVirtualSurface method [DirectComposition]","IDCompositionDevice interface","DXGI_ALPHA_MODE_IGNORE","DXGI_ALPHA_MODE_PREMULTIPLIED","DXGI_ALPHA_MODE_UNSPECIFIED","IDCompositionDevice interface [DirectComposition]","CreateVirtualSurface method","IDCompositionDevice.CreateVirtualSurface","IDCompositionDevice::CreateVirtualSurface","dcomp/IDCompositionDevice::CreateVirtualSurface","directcomp.idcompositiondevice_createvirtualsurface"]
old-location: directcomp\idcompositiondevice_createvirtualsurface.htm
tech.root: directcomp
ms.assetid: 85619C69-F5AE-4F07-AE56-7305BBECD58F
ms.date: 06/23/2022
ms.keywords: CreateVirtualSurface, CreateVirtualSurface method [DirectComposition], CreateVirtualSurface method [DirectComposition],IDCompositionDevice interface, DXGI_ALPHA_MODE_IGNORE, DXGI_ALPHA_MODE_PREMULTIPLIED, DXGI_ALPHA_MODE_UNSPECIFIED, IDCompositionDevice interface [DirectComposition],CreateVirtualSurface method, IDCompositionDevice.CreateVirtualSurface, IDCompositionDevice::CreateVirtualSurface, dcomp/IDCompositionDevice::CreateVirtualSurface, directcomp.idcompositiondevice_createvirtualsurface
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
 - IDCompositionDevice::CreateVirtualSurface
 - dcomp/IDCompositionDevice::CreateVirtualSurface
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
 - IDCompositionDevice.CreateVirtualSurface
---

# IDCompositionDevice::CreateVirtualSurface


## -description

        Creates a sparsely populated surface that can be associated with one or more visuals for composition.

## -parameters

### -param initialWidth [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The width of the surface, in pixels. The maximum width is 16,777,216 pixels.

### -param initialHeight [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The height of the surface, in pixels. The maximum height is 16,777,216 pixels.

### -param pixelFormat [in]

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>

The pixel format of the surface.

### -param alphaMode [in]

Type: <b><a href="/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode">DXGI_ALPHA_MODE</a></b>

The meaning of the alpha channel, if the pixel format contains an alpha channel. It can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DXGI_ALPHA_MODE_UNSPECIFIED"></a><a id="dxgi_alpha_mode_unspecified"></a><dl>
<dt><b>DXGI_ALPHA_MODE_UNSPECIFIED</b></dt>
</dl>
</td>
<td width="60%">
The alpha channel is not specified. This value has the same effect as <b>DXGI_ALPHA_MODE_IGNORE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="DXGI_ALPHA_MODE_PREMULTIPLIED"></a><a id="dxgi_alpha_mode_premultiplied"></a><dl>
<dt><b>DXGI_ALPHA_MODE_PREMULTIPLIED</b></dt>
</dl>
</td>
<td width="60%">
The color channels contain values that are premultiplied with the alpha channel.


</td>
</tr>
<tr>
<td width="40%"><a id="DXGI_ALPHA_MODE_IGNORE"></a><a id="dxgi_alpha_mode_ignore"></a><dl>
<dt><b>DXGI_ALPHA_MODE_IGNORE</b></dt>
</dl>
</td>
<td width="60%">
The alpha channel should be ignored and the bitmap should be rendered opaquely.

</td>
</tr>
</table>

### -param virtualSurface [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvirtualsurface">IDCompositionVirtualSurface</a>**</b>

The newly created surface object. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

A Microsoft DirectComposition sparse surface is a logical object that behaves like a rectangular array of pixels that can be associated with a visual for composition. The surface is not necessarily backed by any physical video or system memory for every one of its pixels. The application can realize or virtualize parts of the logical surface at different times.



A newly created surface object is in an uninitialized state. While it is uninitialized, the surface has no effect on the composition of the visual tree. It behaves exactly like a surface that is initialized with 100% transparent pixels. 

To initialize the surface with pixel data, use the <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-begindraw">IDCompositionSurface::BeginDraw</a> method. This method not only provides pixels for the surface, but it also allocates actual storage space for those pixels. The memory allocation persists until the application returns some of the memory to the system. The application can free part or all of the allocated memory by calling the <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvirtualsurface-trim">IDComposition::VirtualSurfaceTrim</a> method.



DirectComposition surfaces support the following pixel formats:

<ul>
<li><b>DXGI_FORMAT_B8G8R8A8_UNORM</b></li>
<li><b>DXGI_FORMAT_R8G8B8A8_UNORM</b></li>
<li><b>DXGI_FORMAT_R16G16B16A16_FLOAT</b></li>
</ul>
This method fails if <i>initialWidth</i> or <i>initialHeight</i> exceeds 16,777,216 pixels. 


#### Examples

The following example shows how to create a virtual surface and associate it with a visual.


```cpp
HRESULT RenderAVisual(IDCompositionDevice *pDCompDevice, HWND hwndTarget,
                         UINT surfaceWidth, UINT surfaceHeight) 
{
    // Validate the input parameters.
    if (pDCompDevice == nullptr || hwndTarget == NULL)
        return E_INVALIDARG;
    
    HRESULT hr = S_OK;
    IDCompositionTarget *pTargetWindow = nullptr;
    IDCompositionVisual *pVisual = nullptr;
    IDCompositionVirtualSurface *pVirtualSurface = nullptr;
    ID3D10Texture2D *pTex2D = nullptr;
    POINT offset = {0};

    // Create the rendering target. 
    hr = pDCompDevice->CreateTargetForHwnd(hwndTarget, TRUE, &pTargetWindow);

    if (SUCCEEDED(hr))
    {
        // Create a visual.
        hr = pDCompDevice->CreateVisual(&pVisual);
    }

    if (SUCCEEDED(hr))
    {
        // Add the visual to the root of the composition tree.
        hr = pTargetWindow->SetRoot(pVisual);
    }

    if (SUCCEEDED(hr))
    {
        // Create a virtual surface.
        hr = pDCompDevice->CreateVirtualSurface(surfaceWidth, surfaceHeight, 
            DXGI_FORMAT_R8G8B8A8_UNORM, DXGI_ALPHA_MODE_IGNORE, 
            &pVirtualSurface);
    }

    if (SUCCEEDED(hr))
    {
        // Set the virtual surface as the content of the visual.
        hr = pVisual->SetContent(pVirtualSurface);
    }
    
    if (SUCCEEDED(hr))
    {
        // Retrieve and interface pointer for draw on the surface.
        hr = pVirtualSurface->BeginDraw(NULL, __uuidof(ID3D10Texture2D), 
            (void **) &pTex2D, &offset);
    }

    //
    // TODO: Draw on the surface.
    //
    
    if (SUCCEEDED(hr))
    {
        // Complete the updates to the surface.
        hr = pVirtualSurface->EndDraw();
    }

    // Commit the composition for rendering.
    hr = pDCompDevice->Commit();

    // Clean up.
    SafeRelease(&pTargetWindow);
    SafeRelease(&pVisual);
    SafeRelease(&pVirtualSurface);
    SafeRelease(&pTex2D);

    return hr;

}

```

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-createsurface">IDCompositionDevice::CreateSurface</a>