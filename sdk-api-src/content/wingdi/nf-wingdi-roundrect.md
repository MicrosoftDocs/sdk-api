---
UID: NF:wingdi.RoundRect
title: RoundRect function
author: windows-sdk-content
description: The RoundRect function draws a rectangle with rounded corners. The rectangle is outlined by using the current pen and filled by using the current brush.
old-location: gdi\roundrect.htm
old-project: gdi
ms.assetid: 17808a6a-7bd0-4fd6-81ab-00d5db764b93
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: RoundRect, RoundRect function [Windows GDI], _win32_RoundRect, gdi.roundrect, wingdi/RoundRect
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32Full.dll
api_name:
-	RoundRect
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# RoundRect function


## -description


The <b>RoundRect</b> function draws a rectangle with rounded corners. The rectangle is outlined by using the current pen and filled by using the current brush.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param left

TBD


### -param top

TBD


### -param right

TBD


### -param bottom

TBD


### -param width

TBD


### -param height

TBD




#### - nBottomRect [in]

The y-coordinate, in logical coordinates, of the lower-right corner of the rectangle.


#### - nHeight [in]

The height, in logical coordinates, of the ellipse used to draw the rounded corners.


#### - nLeftRect [in]

The x-coordinate, in logical coordinates, of the upper-left corner of the rectangle.


#### - nRightRect [in]

The x-coordinate, in logical coordinates, of the lower-right corner of the rectangle.


#### - nTopRect [in]

The y-coordinate, in logical coordinates, of the upper-left corner of the rectangle.


#### - nWidth [in]

The width, in logical coordinates, of the ellipse used to draw the rounded corners.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The current position is neither used nor updated by this function.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/c5fc3346-e5d7-49c0-979b-10d91ab965c5">Using Filled Shapes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/8909e85d-fa5b-4058-9e58-e027160ec381">Filled Shape Functions</a>



<a href="https://msdn.microsoft.com/78439288-a769-4aab-aee7-7a03396ccebc">Filled Shapes Overview</a>



<a href="https://msdn.microsoft.com/ed6b9824-1edc-4510-b9da-a4287845aa83">
        Rectangle
      </a>
 

 

