---
UID: NF:dwmapi.DwmExtendFrameIntoClientArea
title: DwmExtendFrameIntoClientArea function
author: windows-sdk-content
description: Extends the window frame into the client area.
old-location: dwm\dwmextendframeintoclientarea.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmextendframeintoclientarea.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DwmExtendFrameIntoClientArea, DwmExtendFrameIntoClientArea function [Desktop Window Manager], _udwm_dwmextendframeintoclientarea, _udwm_dwmextendframeintoclientarea_cpp, dwm.dwmextendframeintoclientarea, dwmapi/DwmExtendFrameIntoClientArea, winui._udwm_dwmextendframeintoclientarea
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - DwmExtendFrameIntoClientArea
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DwmExtendFrameIntoClientArea function


## -description


Extends the window frame into the client area.


## -parameters




### -param hWnd

The handle to the window in which the frame will be extended into the client area.


### -param pMarInset [in]

A pointer to a <a href="inet_MARGINS">MARGINS</a> structure that describes the margins to use when extending the frame into the client area.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function must be called whenever Desktop Window Manager (DWM) composition is toggled. Handle the <a href="https://msdn.microsoft.com/ae412d35-8901-4521-a954-239864bca219">WM_DWMCOMPOSITIONCHANGED</a> message for composition change notification. 

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




<a href="https://msdn.microsoft.com/bdf0f8bd-e399-4244-ae39-460f09a16f3c">DWM Blur Behind Overview</a>
 

 

