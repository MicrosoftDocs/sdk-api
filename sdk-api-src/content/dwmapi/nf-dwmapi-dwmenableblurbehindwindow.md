---
UID: NF:dwmapi.DwmEnableBlurBehindWindow
title: DwmEnableBlurBehindWindow function (dwmapi.h)
description: Enables the blur effect on a specified window.
helpviewer_keywords: ["DwmEnableBlurBehindWindow","DwmEnableBlurBehindWindow function [Desktop Window Manager]","_udwm_dwmenableblurbehindwindow","_udwm_dwmenableblurbehindwindow_cpp","dwm.dwmenableblurbehindwindow","dwmapi/DwmEnableBlurBehindWindow","winui._udwm_dwmenableblurbehindwindow"]
old-location: dwm\dwmenableblurbehindwindow.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmenableblurbehindwindow.htm
ms.date: 12/05/2018
ms.keywords: DwmEnableBlurBehindWindow, DwmEnableBlurBehindWindow function [Desktop Window Manager], _udwm_dwmenableblurbehindwindow, _udwm_dwmenableblurbehindwindow_cpp, dwm.dwmenableblurbehindwindow, dwmapi/DwmEnableBlurBehindWindow, winui._udwm_dwmenableblurbehindwindow
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DwmEnableBlurBehindWindow
 - dwmapi/DwmEnableBlurBehindWindow
dev_langs:
 - c++
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
---

## -description

Enables the blur effect on a specified window.

## -parameters

### -param hWnd [in]

The handle to the window on which the blur-behind data is applied.

### -param pBlurBehind [in]

A pointer to a <a href="/windows/win32/api/dwmapi/ns-dwmapi-dwm_blurbehind">DWM_BLURBEHIND</a> structure that provides blur-behind data.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

> [!NOTE]
> Beginning with Windows 8, calling this function doesn't result in the blur effect, due to a style change in the way windows are rendered.

Enable blur by setting the <b>fEnable</b> member of the <a href="/windows/win32/api/dwmapi/ns-dwmapi-dwm_blurbehind">DWM_BLURBEHIND</a> structure to <b>TRUE</b>. This results in subsequent compositions of the window blurring the content behind it. This function should be called immediately before a <a href="/windows/win32/api/winuser/nf-winuser-beginpaint">BeginPaint</a> call to ensure prompt application of the effect.

The alpha values in the window are honored, and the rendering atop the blur will use these alpha values. It's your application's responsibility to ensure that the alpha values of all pixels in the window are correct. Some Windows Graphics Device Interface (GDI) operations don't preserve alpha values, so you should take care when presenting child windows because the alpha values they contribute are unpredictable.

The region specified within the <a href="/windows/win32/api/dwmapi/ns-dwmapi-dwm_blurbehind">DWM_BLURBEHIND</a> structure is owned by you as the caller. It's the caller's responsibility to free the region, and you can do so as soon as the function call is completed.

This function can be called only on top-level windows. An error occurs when this function is called on other window types.

This function must be called whenever Desktop Window Manager (DWM) composition is toggled. Handle the <a href="/windows/win32/dwm/wm-dwmcompositionchanged">WM_DWMCOMPOSITIONCHANGED</a> message for composition change notification.

## Examples

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

[DWM Blur Behind Overview](/windows/win32/dwm/blur-ovw)

