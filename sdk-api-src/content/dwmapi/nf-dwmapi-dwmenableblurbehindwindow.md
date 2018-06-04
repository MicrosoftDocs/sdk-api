---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# DwmEnableBlurBehindWindow function


## -description


Enables the blur effect on a specified window.


## -parameters




### -param hWnd

The handle to the window on which the blur behind data is applied.


### -param pBlurBehind [in]

A pointer to a <a href="https://msdn.microsoft.com/b48698dc-dca1-44c0-935d-43fcba9130f5">DWM_BLURBEHIND</a> structure that provides blur behind data.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Enabling blur by setting the <b>fEnable</b> member of the <a href="https://msdn.microsoft.com/b48698dc-dca1-44c0-935d-43fcba9130f5">DWM_BLURBEHIND</a> structure to <b>TRUE</b>. This results in subsequent compositions of the window blurring the content behind it. This function should be called immediately before a <a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a> call to ensure prompt application of the effect.

The alpha values in the window are honored and the rendering atop the blur will use these alpha values. It is the application's responsibility to ensure that the alpha values of all pixels in the window are correct. Some Windows Graphics Device Interface (GDI) operations do not preserve alpha values, so care must be taken when presenting child windows because the alpha values they contribute are unpredictable.

The region specified within the <a href="https://msdn.microsoft.com/b48698dc-dca1-44c0-935d-43fcba9130f5">DWM_BLURBEHIND</a> structure is owned by the caller. It is the caller's responsibility to free the region, and they can do so as soon as the function call is completed.

This function can only be called on top-level windows. An error occurs when this function is called on other window types.

This function must be called whenver Desktop Window Manager (DWM) composition is toggled. Handle the <a href="https://msdn.microsoft.com/ae412d35-8901-4521-a954-239864bca219">WM_DWMCOMPOSITIONCHANGED</a> message for composition change notification.


#### Examples

The following example demonstrates how to apply the blur behind the entire window.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT EnableBlurBehind(HWND hwnd)
{
   HRESULT hr = S_OK;

   // Create and populate the Blur Behind structure
   DWM_BLURBEHIND bb = {0};

   // Enable Blur Behind and apply to the entire client area
   bb.dwFlags = DWM_BB_ENABLE;
   bb.fEnable = true;
   bb.hRgnBlur = NULL;

   // Apply Blur Behind
   hr = DwmEnableBlurBehindWindow(hwnd, &amp;bb);
   if (SUCCEEDED(hr))
   {
      // ...
   }
   return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bdf0f8bd-e399-4244-ae39-460f09a16f3c">DWM Blur Behind Overview</a>
 

 

