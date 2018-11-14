---
UID: NF:dcomp.DCompositionCreateDevice
title: DCompositionCreateDevice function
author: windows-sdk-content
description: Creates a new device object that can be used to create other Microsoft DirectComposition objects.
old-location: directcomp\dcompositioncreatedevice.htm
tech.root: directcomp
ms.assetid: 3eb5d698-3cbf-456e-aa5f-395687c68c13
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: DCompositionCreateDevice, DCompositionCreateDevice function [DirectComposition], dcomp/DCompositionCreateDevice, directcomp.dcompositioncreatedevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dcomp.dll
api_name:
 - DCompositionCreateDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DCompositionCreateDevice
: 
---

# DCompositionCreateDevice function


## -description


Creates a new device object that can be used to create other Microsoft DirectComposition objects.


## -parameters




### -param dxgiDevice [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb174527(v=VS.85).aspx">IDXGIDevice</a>*</b>

The DXGI device to use to create DirectComposition surface objects.


### -param iid [in]

Type: <b>REFIID</b>

The identifier of the interface to retrieve. 


### -param dcompositionDevice [out]

Type: <b>void**</b>

Receives an interface pointer to the newly created device object. The pointer is of the type specified by the <i>iid</i> parameter. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



A  device object serves as the factory for all other DirectComposition objects. It also controls transactional composition through the <a href="https://msdn.microsoft.com/49a6d33d-7454-44be-b8ca-602b247d4eab">IDCompositionDevice::Commit</a> method.

The DXGI device specified by <i>dxgiDevice</i> is used to create all DirectComposition surface objects. In particular, the <a href="https://msdn.microsoft.com/0D7E90A1-90E4-44BE-A4DA-8DA300C81A35">IDCompositionSurface::BeginDraw</a> method returns an interface pointer to a DXGI surface that belongs to the device specified by the <i>dxgiDevice</i> parameter.



When creating the DXGI device, developers must specify the <a href="https://msdn.microsoft.com/580c784a-17de-495c-9159-833f858ad155">D3D11_CREATE_DEVICE BGRA_SUPPORT</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb204909(v=VS.85).aspx">D3D10_CREATE_DEVICE_BGRA_SUPPORT</a> flag for Direct2D interoperability with Microsoft Direct3D resources.

The <i>iid</i> parameter must be <code>__uuidof(IDCompositionDevice)</code>, and the <i>dcompositionDevice</i> parameter receives a pointer to an <a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a> interface.



#### Examples

The following example shows how to create a device object as part of initialing DirectComposition objects.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;dcomp.h&gt;
#include &lt;d3d11.h&gt;

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
        &amp;featureLevelSupported,
        NULL);

    if (SUCCEEDED(hr))
    {
        // Create the DXGI device used to create bitmap surfaces.
        hr = (*ppD3D11Device)-&gt;QueryInterface(&amp;pDXGIDevice);
    }

    if (SUCCEEDED(hr))
    {
        // Create the DirectComposition device object.
        hr = DCompositionCreateDevice(pDXGIDevice, __uuidof(IDCompositionDevice), 
                reinterpret_cast&lt;void **&gt;(ppDevice));
    }

    if (SUCCEEDED(hr))
    {
        // Bind the DirectComposition device to the target window.
        hr = (*ppDevice)-&gt;CreateTargetForHwnd(hwndTarget, TRUE, ppCompTarget);   
    }

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/750FDFD5-ADD5-43B3-A596-ECDB82C2EF73">Functions</a>
 

 

