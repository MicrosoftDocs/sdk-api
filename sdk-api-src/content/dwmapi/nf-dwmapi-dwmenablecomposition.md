---
UID: NF:dwmapi.DwmEnableComposition
title: DwmEnableComposition function
author: windows-sdk-content
description: Enables or disables Desktop Window Manager (DWM) composition.
old-location: dwm\dwmenablecomposition.htm
old-project: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmenablecomposition.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DwmEnableComposition, DwmEnableComposition function [Desktop Window Manager], _udwm_dwmenablecomposition, _udwm_dwmenablecomposition_cpp, dwm.dwmenablecomposition, dwmapi/DwmEnableComposition, winui._udwm_dwmenablecomposition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dwmapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dwmapi.dll
api_name:
 - DwmEnableComposition
product: Windows
targetos: Windows
req.lib: Dwmapi.lib
req.dll: Dwmapi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DwmEnableComposition function


## -description


Enables or disables Desktop Window Manager (DWM) composition.
        
            
<div class="alert"><b>Note</b>  This function is deprecated as of Windows 8. DWM can no longer be programmatically disabled.</div><div> </div>

## -parameters




### -param uCompositionAction

<b>DWM_EC_ENABLECOMPOSITION</b> to enable DWM composition; <b>DWM_EC_DISABLECOMPOSITION</b> to disable composition.
                        

<div class="alert"><b>Note</b>  As of Windows 8, calling this function with <b>DWM_EC_DISABLECOMPOSITION</b> has no effect. However, the function will still return a success code.</div>
<div> </div>

## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Disabling DWM composition disables it for the entire desktop. DWM composition will be automatically enabled when all processes that have disabled composition have called <b>DwmEnableComposition</b> to enable it or have been terminated. The <a href="https://msdn.microsoft.com/ae412d35-8901-4521-a954-239864bca219">WM_DWMCOMPOSITIONCHANGED</a> notification is sent whenever DWM composition is enabled or disabled.


#### Examples

The following code example disables DWM composition.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
...
HRESULT hr = S_OK;

// Disable DWM Composition 
hr = DwmEnableComposition(DWM_EC_DISABLECOMPOSITION);
if (SUCCEEDED(hr))
{
   // ...
}
...</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b728db22-db83-4607-8b09-6967697ef1b0">Enable and Control DWM Composition</a>
 

 

