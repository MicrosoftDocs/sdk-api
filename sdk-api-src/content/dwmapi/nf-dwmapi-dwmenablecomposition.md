---
UID: NF:dwmapi.DwmEnableComposition
title: DwmEnableComposition function (dwmapi.h)
description: Enables or disables Desktop Window Manager (DWM) composition.
helpviewer_keywords: ["DwmEnableComposition","DwmEnableComposition function [Desktop Window Manager]","_udwm_dwmenablecomposition","_udwm_dwmenablecomposition_cpp","dwm.dwmenablecomposition","dwmapi/DwmEnableComposition","winui._udwm_dwmenablecomposition"]
old-location: dwm\dwmenablecomposition.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmenablecomposition.htm
ms.date: 12/05/2018
ms.keywords: DwmEnableComposition, DwmEnableComposition function [Desktop Window Manager], _udwm_dwmenablecomposition, _udwm_dwmenablecomposition_cpp, dwm.dwmenablecomposition, dwmapi/DwmEnableComposition, winui._udwm_dwmenablecomposition
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
 - DwmEnableComposition
 - dwmapi/DwmEnableComposition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dwmapi.dll
api_name:
 - DwmEnableComposition
---

# DwmEnableComposition function


## -description

Enables or disables Desktop Window Manager (DWM) composition.
        
            
<div class="alert"><b>Note</b>  This function is deprecated as of Windows 8. DWM can no longer be programmatically disabled.</div><div> </div>

## -parameters

### -param uCompositionAction [in]

<b>DWM_EC_ENABLECOMPOSITION</b> to enable DWM composition; <b>DWM_EC_DISABLECOMPOSITION</b> to disable composition.
                        

<div class="alert"><b>Note</b>  As of Windows 8, calling this function with <b>DWM_EC_DISABLECOMPOSITION</b> has no effect. However, the function will still return a success code.</div>
<div> </div>

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Disabling DWM composition disables it for the entire desktop. DWM composition will be automatically enabled when all processes that have disabled composition have called <b>DwmEnableComposition</b> to enable it or have been terminated. The <a href="/windows/desktop/dwm/wm-dwmcompositionchanged">WM_DWMCOMPOSITIONCHANGED</a> notification is sent whenever DWM composition is enabled or disabled.


#### Examples

The following code example disables DWM composition.


```cpp

...
HRESULT hr = S_OK;

// Disable DWM Composition 
hr = DwmEnableComposition(DWM_EC_DISABLECOMPOSITION);
if (SUCCEEDED(hr))
{
   // ...
}
...
```

## -see-also

<a href="/windows/desktop/dwm/composition-ovw">Enable and Control DWM Composition</a>