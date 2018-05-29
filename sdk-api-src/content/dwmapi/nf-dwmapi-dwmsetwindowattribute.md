---
UID: NF:dwmapi.DwmSetWindowAttribute
title: DwmSetWindowAttribute function
author: windows-sdk-content
description: Sets the value of non-client rendering attributes for a window.
old-location: dwm\dwmsetwindowattribute.htm
old-project: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmsetwindowattribute.htm
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: DwmSetWindowAttribute, DwmSetWindowAttribute function [Desktop Window Manager], _udwm_dwmsetwindowattribute, _udwm_dwmsetwindowattribute_cpp, dwm.dwmsetwindowattribute, dwmapi/DwmSetWindowAttribute, winui._udwm_dwmsetwindowattribute
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dwmapi.dll
-	uxtheme.dll
-	ext-ms-win-dwmapi-ext-l1-1-0.dll
api_name:
-	DwmSetWindowAttribute
product: Windows
targetos: Windows
req.lib: Dwmapi.lib
req.dll: Dwmapi.dll; Uxtheme.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DwmSetWindowAttribute function


## -description


Sets the value of non-client rendering attributes for a window.


## -parameters




### -param hwnd

The handle to the window that will receive the attributes.


### -param dwAttribute

A single <a href="https://msdn.microsoft.com/f7ed01d1-b5c6-4071-906b-1647ffa2157c">DWMWINDOWATTRIBUTE</a> flag to apply to the window. This parameter specifies the attribute and the <i>pvAttribute</i> parameter points to the value of that attribute.


### -param pvAttribute [in]

A pointer to the value of the attribute specified in the <i>dwAttribute</i> parameter. Different <a href="https://msdn.microsoft.com/f7ed01d1-b5c6-4071-906b-1647ffa2157c">DWMWINDOWATTRIBUTE</a> flags require different value types.


### -param cbAttribute

The size, in bytes, of the value type pointed to by the <i>pvAttribute</i> parameter.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Calling this function with the <i>dwAttribute</i> set to <b>DWMWA_NCRENDERING_ENABLED</b> does not set the attribute. <b>DWMWA_NCRENDERING_ENABLED</b> is a "get" attribute and the resulting call is equivalent to a <a href="https://msdn.microsoft.com/1b08de95-703f-4f61-9341-97124a3072f2">DwmGetWindowAttribute</a> call. To enable or disable non-client rendering, the <b>DWMWA_NCRENDERING_POLICY</b> attribute must set to the desired value.

If Desktop Composition has been disabled, this function returns <b>DWM_E_COMPOSITIONDISABLED</b>.


#### Examples

The following example disables nonclient-area rendering, causing any previous calls to <a href="https://msdn.microsoft.com/e4b99f11-cab0-4713-8112-aab93c78378d">DwmEnableBlurBehindWindow</a> or <a href="https://msdn.microsoft.com/4ea409df-3980-4903-b481-6ff718dc01bc">DwmExtendFrameIntoClientArea</a> to be disabled.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT DisableNCRendering(HWND hwnd)
{
   HRESULT hr = S_OK;
   DWMNCRENDERINGPOLICY ncrp = DWMNCRP_DISABLED;

   // Disable non-client area rendering on the window.
   hr = DwmSetWindowAttribute(hwnd, DWMWA_NCRENDERING_POLICY, &amp;ncrp, sizeof(ncrp));

   if (SUCCEEDED(hr))
   {
      // Do work here. 
   }
 
   return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b728db22-db83-4607-8b09-6967697ef1b0">Enable and Control DWM Composition</a>
 

 

