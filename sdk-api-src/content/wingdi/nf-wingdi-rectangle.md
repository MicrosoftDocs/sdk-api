---
UID: NF:wingdi.Rectangle
title: Rectangle function
author: windows-sdk-content
description: The Rectangle function draws a rectangle. The rectangle is outlined by using the current pen and filled by using the current brush.
old-location: gdi\rectangle.htm
tech.root: gdi
ms.assetid: ed6b9824-1edc-4510-b9da-a4287845aa83
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Rectangle, Rectangle function [Windows GDI], _win32_Rectangle, gdi.rectangle, wingdi/Rectangle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wingdi.h
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - Rectangle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Rectangle function


## -description


The <b>Rectangle</b> function draws a rectangle. The rectangle is outlined by using the current pen and filled by using the current brush.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param left [in]

The x-coordinate, in logical coordinates, of the upper-left corner of the rectangle.


### -param top [in]

The y-coordinate, in logical coordinates, of the upper-left corner of the rectangle.


### -param right [in]

The x-coordinate, in logical coordinates, of the lower-right corner of the rectangle.


### -param bottom [in]

The y-coordinate, in logical coordinates, of the lower-right corner of the rectangle.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The current position is neither used nor updated by <b>Rectangle</b>.

The rectangle that is drawn excludes the bottom and right edges.

If a PS_NULL pen is used, the dimensions of the rectangle are 1 pixel less in height and 1 pixel less in width.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/c5fc3346-e5d7-49c0-979b-10d91ab965c5">Using Filled Shapes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/8909e85d-fa5b-4058-9e58-e027160ec381">Filled Shape Functions</a>



<a href="https://msdn.microsoft.com/78439288-a769-4aab-aee7-7a03396ccebc">Filled Shapes Overview</a>



<a href="https://msdn.microsoft.com/17808a6a-7bd0-4fd6-81ab-00d5db764b93">RoundRect
      </a>
 

 

