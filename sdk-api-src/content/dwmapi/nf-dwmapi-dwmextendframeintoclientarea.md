---
UID: NF:dwmapi.DwmExtendFrameIntoClientArea
title: DwmExtendFrameIntoClientArea function (dwmapi.h)
description: Extends the window frame into the client area.
helpviewer_keywords: ["DwmExtendFrameIntoClientArea","DwmExtendFrameIntoClientArea function [Desktop Window Manager]","_udwm_dwmextendframeintoclientarea","_udwm_dwmextendframeintoclientarea_cpp","dwm.dwmextendframeintoclientarea","dwmapi/DwmExtendFrameIntoClientArea","winui._udwm_dwmextendframeintoclientarea"]
old-location: dwm\dwmextendframeintoclientarea.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmextendframeintoclientarea.htm
ms.date: 12/05/2018
ms.keywords: DwmExtendFrameIntoClientArea, DwmExtendFrameIntoClientArea function [Desktop Window Manager], _udwm_dwmextendframeintoclientarea, _udwm_dwmextendframeintoclientarea_cpp, dwm.dwmextendframeintoclientarea, dwmapi/DwmExtendFrameIntoClientArea, winui._udwm_dwmextendframeintoclientarea
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
 - DwmExtendFrameIntoClientArea
 - dwmapi/DwmExtendFrameIntoClientArea
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
 - ext-ms-win-dwmapi-ext-l1-1-1.dll
 - ext-ms-win-dwmapi-ext-l1-1-2.dll
api_name:
 - DwmExtendFrameIntoClientArea
---

# DwmExtendFrameIntoClientArea function


## -description

Extends the window frame into the client area.

## -parameters

### -param hWnd [in]

The handle to the window in which the frame will be extended into the client area.

### -param pMarInset [in]

A pointer to a <a href="/windows/desktop/api/uxtheme/ns-uxtheme-margins">MARGINS</a> structure that describes the margins to use when extending the frame into the client area.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function must be called whenever Desktop Window Manager (DWM) composition is toggled. Handle the <a href="/windows/desktop/dwm/wm-dwmcompositionchanged">WM_DWMCOMPOSITIONCHANGED</a> message for composition change notification. 

Use negative margin values to create the "sheet of glass" effect where the client area is rendered as a solid surface with no window border.


#### Examples

The following sample demonstrates how to extend the bottom margin, creating a large bottom frame.


```cpp

HRESULT ExtendIntoClientBottom(HWND hwnd)
{
   // Set margins, extending the bottom margin
   MARGINS margins = {0,0,0,25};
   HRESULT hr = S_OK;

   // Extend frame on the bottom of client area
   hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
   if (SUCCEEDED(hr))
   {
      // ...
   }
   return hr;
}
```


The following sample demonstrates the "sheet of glass" effect where the client area is rendered without a window border.


```cpp

HRESULT ExtendIntoClientAll(HWND hwnd)
{
   // Negative margins have special meaning to DwmExtendFrameIntoClientArea.
   // Negative margins create the "sheet of glass" effect, where the client area
   // is rendered as a solid surface with no window border.
   MARGINS margins = {-1};
   HRESULT hr = S_OK;

   // Extend the frame across the entire window.
   hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
   if (SUCCEEDED(hr))
   {
      // ...
   }
   return hr;
}
```

## -see-also

<a href="/windows/desktop/dwm/blur-ovw">DWM Blur Behind Overview</a>