---
UID: NF:uiribbon.IUIRibbon.GetHeight
title: IUIRibbon::GetHeight (uiribbon.h)
description: Retrieves the height of the ribbon.
helpviewer_keywords: ["GetHeight","GetHeight method [Windows Ribbon]","GetHeight method [Windows Ribbon]","IUIRibbon interface","IUIRibbon interface [Windows Ribbon]","GetHeight method","IUIRibbon.GetHeight","IUIRibbon::GetHeight","scenicintent_IUIRibbon_GetHeight","uiribbon/IUIRibbon::GetHeight","windowsribbon.windowsribbon_iuiribbon_getheight"]
old-location: windowsribbon\windowsribbon_iuiribbon_getheight.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiribbon\getheight.htm
ms.date: 12/05/2018
ms.keywords: GetHeight, GetHeight method [Windows Ribbon], GetHeight method [Windows Ribbon],IUIRibbon interface, IUIRibbon interface [Windows Ribbon],GetHeight method, IUIRibbon.GetHeight, IUIRibbon::GetHeight, scenicintent_IUIRibbon_GetHeight, uiribbon/IUIRibbon::GetHeight, windowsribbon.windowsribbon_iuiribbon_getheight
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: Windows UI
ms.custom: 19H1
f1_keywords:
 - IUIRibbon::GetHeight
 - uiribbon/IUIRibbon::GetHeight
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mshtml.dll
api_name:
 - IUIRibbon.GetHeight
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The value returned for <i>cy</i> is based on a number of dependencies that
			include, but are not limited to, the width of the host window and the layout template declared 
			in the Ribbon markup. 
			


#### Examples

The following example demonstrates how to use the <b>IUIRibbon::GetHeight</b> method to retrieve the height  of the ribbon to calculate a display location for a <a href="/windows/desktop/windowsribbon/windowsribbon-controls-contextpopup">Context Popup</a> control.


```cpp
void GetDisplayLocation(POINT &pt, HWND hWnd)
{
  if (pt.x == -1 && pt.y == -1)
  {
    HRESULT hr = E_FAIL;

    // Display the menu in the upper-left corner of the client area, below the ribbon.
    IUIRibbon* pRibbon;
    hr = g_pFramework->GetView(0, IID_PPV_ARGS(&pRibbon));
    if (SUCCEEDED(hr))
    {
      UINT32 uRibbonHeight = 0;
      hr = pRibbon->GetHeight(&uRibbonHeight);
      if (SUCCEEDED(hr))
      {
        pt.x = 0;
        pt.y = uRibbonHeight;
        // Convert client coordinates of a specified point to screen coordinates.
        ClientToScreen(hWnd, &pt);
      }
      pRibbon->Release();
    }
    if (FAILED(hr))
    {
      // Default to just the upper-right corner of the entire screen.
      pt.x = 0;
      pt.y = 0;
    }
  }
}
```

## -see-also

<a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon">IUIRibbon</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-samples-entry">Windows Ribbon Framework Samples</a>