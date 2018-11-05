---
UID: NF:winuser.FrameRect
title: FrameRect function
author: windows-sdk-content
description: The FrameRect function draws a border around the specified rectangle by using the specified brush. The width and height of the border are always one logical unit.
old-location: gdi\framerect.htm
tech.root: gdi
ms.assetid: a1083cb5-5e6c-4134-badf-9fc5142d1453
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: FrameRect, FrameRect function [Windows GDI], _win32_FrameRect, gdi.framerect, winuser/FrameRect
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
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-GUI-l1-2-0.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-NTUser-Gui-L1-3-0.dll
api_name:
 - FrameRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FrameRect function


## -description


The <b>FrameRect</b> function draws a border around the specified rectangle by using the specified brush. The width and height of the border are always one logical unit.


## -parameters




### -param hDC [in]

A handle to the device context in which the border is drawn.


### -param lprc [in]

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the logical coordinates of the upper-left and lower-right corners of the rectangle.


### -param hbr [in]

A handle to the brush used to draw the border.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The brush identified by the <i>hbr</i> parameter must have been created by using the <a href="https://msdn.microsoft.com/0b5849d6-1e22-4ac5-980c-2f2a73b16adb">CreateHatchBrush</a>, <a href="https://msdn.microsoft.com/a3cf347e-9803-4bb0-bdb3-98929ef859ab">CreatePatternBrush</a>, or <a href="https://msdn.microsoft.com/e39b5f77-97d8-4ea6-8277-7da12b3367f3">CreateSolidBrush</a> function, or retrieved by using the <a href="https://msdn.microsoft.com/b14ddc05-7e7b-4fc6-b7e3-efe892df7e21">GetStockObject</a> function.

If the <b>bottom</b> member of the <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure is less than the <b>top</b> member, or if the <b>right</b> member is less than the <b>left</b> member, the function does not draw the rectangle.




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
 

 

