---
UID: NF:dwmapi.DwmEnableBlurBehindWindow
title: DwmEnableBlurBehindWindow function (dwmapi.h)
author: windows-sdk-content
description: Enables the blur effect on a specified window.
old-location: dwm\dwmenableblurbehindwindow.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmenableblurbehindwindow.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DwmEnableBlurBehindWindow, DwmEnableBlurBehindWindow function [Desktop Window Manager], _udwm_dwmenableblurbehindwindow, _udwm_dwmenableblurbehindwindow_cpp, dwm.dwmenableblurbehindwindow, dwmapi/DwmEnableBlurBehindWindow, winui._udwm_dwmenableblurbehindwindow
ms.topic: function
req.header: dwmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwmapi.lib
req.dll: Dwmapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dwmapi.dll
 - ext-ms-win-dwmapi-ext-l1-1-0.dll
api_name:
 - DwmEnableBlurBehindWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DwmEnableBlurBehindWindow function


## -description


Enables the blur effect on a specified window.


## -parameters




### -param hWnd

The handle to the window on which the blur behind data is applied.


### -param pBlurBehind [in]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Aa969500(v=VS.85).aspx">DWM_BLURBEHIND</a> structure that provides blur behind data.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Enabling blur by setting the <b>fEnable</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Aa969500(v=VS.85).aspx">DWM_BLURBEHIND</a> structure to <b>TRUE</b>. This results in subsequent compositions of the window blurring the content behind it. This function should be called immediately before a <a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a> call to ensure prompt application of the effect.

The alpha values in the window are honored and the rendering atop the blur will use these alpha values. It is the application's responsibility to ensure that the alpha values of all pixels in the window are correct. Some Windows Graphics Device Interface (GDI) operations do not preserve alpha values, so care must be taken when presenting child windows because the alpha values they contribute are unpredictable.

The region specified within the <a href="https://msdn.microsoft.com/en-us/library/Aa969500(v=VS.85).aspx">DWM_BLURBEHIND</a> structure is owned by the caller. It is the caller's responsibility to free the region, and they can do so as soon as the function call is completed.

This function can only be called on top-level windows. An error occurs when this function is called on other window types.

This function must be called whenver Desktop Window Manager (DWM) composition is toggled. Handle the <a href="https://msdn.microsoft.com/en-us/library/Dd388199(v=VS.85).aspx">WM_DWMCOMPOSITIONCHANGED</a> message for composition change notification.


#### Examples

The following example demonstrates how to apply the blur behind the entire window.


```cpp

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
   hr = DwmEnableBlurBehindWindow(hwnd, &bb);
   if (SUCCEEDED(hr))
   {
      // ...
   }
   return hr;
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa969537(v=VS.85).aspx">DWM Blur Behind Overview</a>
 

 

