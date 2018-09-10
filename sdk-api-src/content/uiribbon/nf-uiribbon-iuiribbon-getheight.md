---
UID: NF:uiribbon.IUIRibbon.GetHeight
title: IUIRibbon::GetHeight
author: windows-sdk-content
description: Retrieves the height of the ribbon.
old-location: windowsribbon\windowsribbon_iuiribbon_getheight.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiribbon\getheight.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetHeight, GetHeight method [Windows Ribbon], GetHeight method [Windows Ribbon],IUIRibbon interface, IUIRibbon interface [Windows Ribbon],GetHeight method, IUIRibbon.GetHeight, IUIRibbon::GetHeight, scenicintent_IUIRibbon_GetHeight, uiribbon/IUIRibbon::GetHeight, windowsribbon.windowsribbon_iuiribbon_getheight
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mshtml.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mshtml.dll
api_name:
 - IUIRibbon.GetHeight
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Windows UI
---

# IUIRibbon::GetHeight


## -description


Retrieves the height of the ribbon.		
		


## -parameters




### -param cy [out]

Type: <b>UINT32*</b>

The height of the ribbon, in pixels.
				


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The value returned for <i>cy</i> is based on a number of dependencies that
			include, but are not limited to, the width of the host window and the layout template declared 
			in the Ribbon markup. 
			


#### Examples

The following example demonstrates how to use the <b>IUIRibbon::GetHeight</b> method to retrieve the height  of the ribbon to calculate a display location for a <a href="https://msdn.microsoft.com/c41b888a-15aa-4c47-ad73-5dc30b5fa6f9">Context Popup</a> control.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>void GetDisplayLocation(POINT &amp;pt, HWND hWnd)
{
  if (pt.x == -1 &amp;&amp; pt.y == -1)
  {
    HRESULT hr = E_FAIL;

    // Display the menu in the upper-left corner of the client area, below the ribbon.
    IUIRibbon* pRibbon;
    hr = g_pFramework-&gt;GetView(0, IID_PPV_ARGS(&amp;pRibbon));
    if (SUCCEEDED(hr))
    {
      UINT32 uRibbonHeight = 0;
      hr = pRibbon-&gt;GetHeight(&amp;uRibbonHeight);
      if (SUCCEEDED(hr))
      {
        pt.x = 0;
        pt.y = uRibbonHeight;
        // Convert client coordinates of a specified point to screen coordinates.
        ClientToScreen(hWnd, &amp;pt);
      }
      pRibbon-&gt;Release();
    }
    if (FAILED(hr))
    {
      // Default to just the upper-right corner of the entire screen.
      pt.x = 0;
      pt.y = 0;
    }
  }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/6a43f17b-dbf6-4c5b-818f-c0dde896de99">IUIRibbon</a>



<a href="https://msdn.microsoft.com/79d092c9-347b-4b8f-8ba4-a8f696ce6a85">Windows Ribbon Framework Samples</a>
 

 

