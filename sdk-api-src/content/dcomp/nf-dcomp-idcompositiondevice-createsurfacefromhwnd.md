---
UID: NF:dcomp.IDCompositionDevice.CreateSurfaceFromHwnd
title: IDCompositionDevice::CreateSurfaceFromHwnd
author: windows-sdk-content
description: Creates a wrapper object that represents the rasterization of a layered window, and that can be associated with a visual for composition.
old-location: directcomp\idcompositiondevice_createsurfacefromhwnd.htm
tech.root: directcomp
ms.assetid: EA49F8EB-FAC8-421E-854D-C4AA81887EB0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateSurfaceFromHwnd, CreateSurfaceFromHwnd method [DirectComposition], CreateSurfaceFromHwnd method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateSurfaceFromHwnd method, IDCompositionDevice.CreateSurfaceFromHwnd, IDCompositionDevice::CreateSurfaceFromHwnd, dcomp/IDCompositionDevice::CreateSurfaceFromHwnd, directcomp.idcompositiondevice_createsurfacefromhwnd
ms.topic: method
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
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionDevice.CreateSurfaceFromHwnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDevice::CreateSurfaceFromHwnd


## -description


Creates a wrapper object that represents the rasterization of a layered window, and that can be associated with a visual for composition.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The handle of the layered window for which to create a  wrapper. A layered window is created by specifying <b>WS_EX_LAYERED</b> when creating the window with the <a href="https://msdn.microsoft.com/en-us/library/ms632680(v=VS.85).aspx">CreateWindowEx</a> function or by setting <b>WS_EX_LAYERED</b> via <a href="https://msdn.microsoft.com/en-us/library/ms633591(v=VS.85).aspx">SetWindowLong</a> after the window has been created.


### -param surface [out]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>**</b>

The new composition surface object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



You can use the <i>surface</i> pointer in calls to the <a href="https://msdn.microsoft.com/en-us/library/Hh449157(v=VS.85).aspx">IDCompositionVisual::SetContent</a> method to set the content of one or more visuals. After setting the content, the visuals compose the contents of the specified layered window as long as the window is layered. If the window is unlayered, the window content disappears from the output of the composition tree. If the window is later re-layered, the window content reappears as long as it is still associated with a visual.

If the window is resized, the affected visuals are re-composed. 

The contents of the window are not cached beyond the life of the window. That is, if the window is destroyed, the affected visuals stop composing the window.


If the window is moved off-screen or resized to zero, the system stops composing the content of visuals. You should use the <a href="https://msdn.microsoft.com/en-us/library/Aa969524(v=VS.85).aspx">DwmSetWindowAttribute</a> function with the <b>DWMWA_CLOAK</b> flag to "cloak" the layered child window when you need to hide the original window while allowing the system to continue to compose the content of the visuals. For more information, see <a href="https://msdn.microsoft.com/8912CCF9-C343-45CB-AB31-55D26C118AF2">How to animate the bitmap of a layered child window</a> and <a href="http://go.microsoft.com/fwlink/p/?linkid=231194">DirectComposition layered child window sample</a>.


#### Examples

The following code snippet creates a wrapper object that represents the rasterization of a layered window.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT hr = S_OK;
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
</pre>
</td>
</tr>
</table></span></div>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh437392(v=VS.85).aspx">IDCompositionDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh437405(v=VS.85).aspx">IDCompositionDevice::CreateSurface</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh437406(v=VS.85).aspx">IDCompositionDevice::CreateSurfaceFromHandle</a>
 

 

