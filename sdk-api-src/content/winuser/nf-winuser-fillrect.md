---
UID: NF:winuser.FillRect
title: FillRect function
author: windows-sdk-content
description: The FillRect function fills a rectangle by using the specified brush. This function includes the left and top borders, but excludes the right and bottom borders of the rectangle.
old-location: gdi\fillrect.htm
tech.root: gdi
ms.assetid: 98ab34da-ea07-4446-a62e-509c849d95f9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FillRect, FillRect function [Windows GDI], _win32_FillRect, gdi.fillrect, winuser/FillRect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-0.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-GUI-l1-2-0.dll
 - api-ms-win-ntuser-ie-gui-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-NTUser-Gui-L1-3-0.dll
api_name:
 - FillRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FillRect function


## -description


The <b>FillRect</b> function fills a rectangle by using the specified brush. This function includes the left and top borders, but excludes the right and bottom borders of the rectangle.


## -parameters




### -param hDC [in]

A handle to the device context.


### -param lprc [in]

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the logical coordinates of the rectangle to be filled.


### -param hbr [in]

A handle to the brush used to fill the rectangle.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The brush identified by the <i>hbr</i> parameter may be either a handle to a logical brush or a color value. If specifying a handle to a logical brush, call one of the following functions to obtain the handle: <a href="https://msdn.microsoft.com/0b5849d6-1e22-4ac5-980c-2f2a73b16adb">CreateHatchBrush</a>, <a href="https://msdn.microsoft.com/a3cf347e-9803-4bb0-bdb3-98929ef859ab">CreatePatternBrush</a>, or <a href="https://msdn.microsoft.com/e39b5f77-97d8-4ea6-8277-7da12b3367f3">CreateSolidBrush</a>. Additionally, you may retrieve a handle to one of the stock brushes by using the <a href="https://msdn.microsoft.com/b14ddc05-7e7b-4fc6-b7e3-efe892df7e21">GetStockObject</a> function. If specifying a color value for the <i>hbr</i> parameter, it must be one of the standard system colors (the value 1 must be added to the chosen color). For example:


```cpp

FillRect(hdc, &rect, (HBRUSH) (COLOR_WINDOW+1));

```


For a list of all the standard system colors, see <a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a>.

When filling the specified rectangle, <b>FillRect</b> does not include the rectangle's right and bottom sides. GDI fills a rectangle up to, but not including, the right column and bottom row, regardless of the current mapping mode.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/e8861240-9345-43e6-820d-d237247d1bd7">Using Rectangles</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0b5849d6-1e22-4ac5-980c-2f2a73b16adb">CreateHatchBrush
      </a>



<a href="https://msdn.microsoft.com/a3cf347e-9803-4bb0-bdb3-98929ef859ab">CreatePatternBrush
      </a>



<a href="https://msdn.microsoft.com/e39b5f77-97d8-4ea6-8277-7da12b3367f3">CreateSolidBrush
      </a>



<a href="https://msdn.microsoft.com/8909e85d-fa5b-4058-9e58-e027160ec381">Filled Shape Functions</a>



<a href="https://msdn.microsoft.com/78439288-a769-4aab-aee7-7a03396ccebc">Filled Shapes Overview</a>



<a href="https://msdn.microsoft.com/b14ddc05-7e7b-4fc6-b7e3-efe892df7e21">GetStockObject
      </a>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT
      </a>
 

 

