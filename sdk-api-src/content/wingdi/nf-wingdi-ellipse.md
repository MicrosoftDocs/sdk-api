---
UID: NF:wingdi.Ellipse
title: Ellipse function
author: windows-driver-content
description: The Ellipse function draws an ellipse. The center of the ellipse is the center of the specified bounding rectangle. The ellipse is outlined by using the current pen and is filled by using the current brush.
old-location: gdi\ellipse.htm
old-project: gdi
ms.assetid: 9bec59dd-6bcb-498e-9ed2-ac641ecd7fa5
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: Ellipse, Ellipse function [Windows GDI], _win32_Ellipse, gdi.ellipse, wingdi/Ellipse
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
-	Ellipse
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# Ellipse function


## -description


The <b>Ellipse</b> function draws an ellipse. The center of the ellipse is the center of the specified bounding rectangle. The ellipse is outlined by using the current pen and is filled by using the current brush.


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




#### - nBottomRect [in]

The y-coordinate, in logical coordinates, of the lower-right corner of the bounding rectangle.


#### - nLeftRect [in]

The x-coordinate, in logical coordinates, of the upper-left corner of the bounding rectangle.


#### - nRightRect [in]

The x-coordinate, in logical coordinates, of the lower-right corner of the bounding rectangle.


#### - nTopRect [in]

The y-coordinate, in logical coordinates, of the upper-left corner of the bounding rectangle.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The current position is neither used nor updated by <b>Ellipse</b>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/c5fc3346-e5d7-49c0-979b-10d91ab965c5">Using Filled Shapes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/c15a2173-0fad-4a8a-b0f9-cd39fe4e7bac">
        Arc
      </a>



<a href="https://msdn.microsoft.com/5e358a14-9f39-4267-9a44-c8bf05b5dfbb">
        ArcTo
      </a>



<a href="https://msdn.microsoft.com/8909e85d-fa5b-4058-9e58-e027160ec381">Filled Shape Functions</a>



<a href="https://msdn.microsoft.com/78439288-a769-4aab-aee7-7a03396ccebc">Filled Shapes Overview</a>
 

 

