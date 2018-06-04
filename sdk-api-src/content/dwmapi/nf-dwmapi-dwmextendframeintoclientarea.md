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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT ExtendIntoClientBottom(HWND hwnd)
{
   // Set margins, extending the bottom margin
   MARGINS margins = {0,0,0,25};
   HRESULT hr = S_OK;

   // Extend frame on the bottom of client area
   hr = DwmExtendFrameIntoClientArea(hwnd,&amp;margins);
   if (SUCCEEDED(hr))
   {
      // ...
   }
   return hr;
}</pre>
</td>
</tr>
</table></span></div>
The following sample demonstrates the "sheet of glass" effect where the client area is rendered without a window border.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT ExtendIntoClientAll(HWND hwnd)
{
   // Negative margins have special meaning to DwmExtendFrameIntoClientArea.
   // Negative margins create the "sheet of glass" effect, where the client area
   // is rendered as a solid surface with no window border.
   MARGINS margins = {-1};
   HRESULT hr = S_OK;

   // Extend the frame across the entire window.
   hr = DwmExtendFrameIntoClientArea(hwnd,&amp;margins);
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
 

 

