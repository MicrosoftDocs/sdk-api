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
 

 

