---
UID: NF:dcomp.IDCompositionDevice.CreateTargetForHwnd
title: IDCompositionDevice::CreateTargetForHwnd
author: windows-sdk-content
description: Creates a composition target object that is bound to the window that is represented by the specified window handle (HWND).
old-location: directcomp\idcompositiondevice_createhwndtarget.htm
old-project: directcomp
ms.assetid: eba2388a-9c94-43f0-bf7f-e814895a2792
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: CreateTargetForHwnd, CreateTargetForHwnd method [DirectComposition], CreateTargetForHwnd method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateTargetForHwnd method, IDCompositionDevice.CreateTargetForHwnd, IDCompositionDevice::CreateTargetForHwnd, dcomp/IDCompositionDevice::CreateTargetForHwnd, directcomp.idcompositiondevice_createhwndtarget
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D2D_VECTOR_4F
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionDevice.CreateTargetForHwnd
product: Windows
targetos: Windows
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
---

# IDCompositionDevice::CreateTargetForHwnd


## -description


Creates a composition target object that is bound to the window that is represented by the specified window handle (<a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a>).


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The window to which the  composition target object should be bound. This parameter must not be NULL.


### -param topmost [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

TRUE if the visual tree should be displayed on top of the children of the window specified by the <i>hwnd</i> parameter; otherwise, the visual tree is displayed behind the children.


### -param target [out]

Type: <b><a href="https://msdn.microsoft.com/86dbfe68-e360-42cf-b572-960398ef06ba">IDCompositionTarget</a>**</b>

The new composition target object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



A Microsoft DirectComposition visual tree must be bound to a window before anything can be displayed on screen. The window can be a top-level window or a child window. In either case, the window can be a layered window, but in all cases the window must belong to the calling process. If the window belongs to a different process, this method returns <a href="directcomposition_error_codes.htm">DCOMPOSITION_ERROR_ACCESS_DENIED</a>. 

When DirectComposition content is composed to the window, the content is always composed on top of whatever is drawn directly to that window through the device context (<a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a>) returned by the <a href="https://msdn.microsoft.com/50b2387b-c8e4-42a8-8f0f-0bdb355adbfd">GetDC</a> function, or by calls to Microsoft DirectX <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">Present</a> methods. However, because window clipping rules apply to DirectComposition content, if the window has child windows, those child windows may clip the visual tree. The <i>topmost</i> parameter determines whether child windows clip the visual tree. 

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




<a href="basic_concepts.htm">Composition Target Window</a>



<a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a>



<a href="https://msdn.microsoft.com/86dbfe68-e360-42cf-b572-960398ef06ba">IDCompositionTarget</a>



<a href="https://msdn.microsoft.com/febbef70-fc21-4295-93c5-2f9f52434aae">IDCompositionTarget::SetRoot</a>



<a href="https://msdn.microsoft.com/462dfc20-ad5a-425c-94b5-f21ab05f5af8">IDCompositionVisual</a>
 

 

