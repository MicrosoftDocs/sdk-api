---
UID: NF:winuser.EndPaint
title: EndPaint function
author: windows-sdk-content
description: The EndPaint function marks the end of painting in the specified window. This function is required for each call to the BeginPaint function, but only after painting is complete.
old-location: gdi\endpaint.htm
tech.root: gdi
ms.assetid: b07cfed9-21c4-4459-855a-eaf4d1d34ab8
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: EndPaint, EndPaint function [Windows GDI], _win32_EndPaint, gdi.endpaint, winuser/EndPaint
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
 - Ext-MS-Win-NTUser-Draw-l1-1-0.dll
 - Ext-MS-Win-NTUser-Draw-l1-1-1.dll
 - ext-ms-win-ntuser-draw-l1-1-2.dll
api_name:
 - EndPaint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EndPaint function


## -description


The <b>EndPaint</b> function marks the end of painting in the specified window. This function is required for each call to the <a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a> function, but only after painting is complete.


## -parameters




### -param hWnd [in]

Handle to the window that has been repainted.


### -param lpPaint [in]

Pointer to a <a href="https://msdn.microsoft.com/1f8c6dd2-e511-48f2-8ab0-d2fadb1ce433">PAINTSTRUCT</a> structure that contains the painting information retrieved by <a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a>.


## -returns



The return value is always nonzero.




## -remarks



If the caret was hidden by <a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a>, <b>EndPaint</b> restores the caret to the screen.

<b>EndPaint</b> releases the display device context that <a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a> retrieved.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/ed995bfd-a791-4d73-9a0b-daf65a9f7709">Drawing in the Client Area</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a>



<a href="https://msdn.microsoft.com/1f8c6dd2-e511-48f2-8ab0-d2fadb1ce433">PAINTSTRUCT</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>
 

 

