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

# DwmGetColorizationColor function


## -description


Retrieves the current color used for Desktop Window Manager (DWM) glass composition. This value is based on the current color scheme and can be modified by the user. Applications can listen for color changes by handling the <a href="https://msdn.microsoft.com/6118d41b-f0b4-4034-aa98-d8757f18ca0d">WM_DWMCOLORIZATIONCOLORCHANGED</a> notification.


## -parameters




### -param pcrColorization [out]

A pointer to a value that, when this function returns successfully, receives the current color used for glass composition. The color format of the value is 0xAARRGGBB.


### -param pfOpaqueBlend [out]

A pointer to a value that, when this function returns successfully, indicates whether the color is an opaque blend. <b>TRUE</b> if the color is an opaque blend; otherwise, <b>FALSE</b>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The value pointed to by <i>pcrColorization</i> is in an 0xAARRGGBB format. Many Microsoft Win32 APIs, such as <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>, use a 0x00BBGGRR format. Be careful to assure that the intended colors are used.


#### Examples

The following example code shows a <a href="https://msdn.microsoft.com/6118d41b-f0b4-4034-aa98-d8757f18ca0d">WM_DWMCOLORIZATIONCOLORCHANGED</a> notification handle. If the colorization notification is received, this code retrieves the new color value.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
...
DWORD color = 0;
BOOL opaque = FALSE;
  
HRESULT hr = DwmGetColorizationColor(&amp;color, &amp;opaque);
if (SUCCEEDED(hr))
{
  // Update the application to use the new color.
}
...</pre>
</td>
</tr>
</table></span></div>


