---
UID: NF:wingdi.Ellipse
title: Ellipse function (wingdi.h)
description: The Ellipse function draws an ellipse. The center of the ellipse is the center of the specified bounding rectangle. The ellipse is outlined by using the current pen and is filled by using the current brush.helpviewer_keywords: ["Ellipse","Ellipse function [Windows GDI]","_win32_Ellipse","gdi.ellipse","wingdi/Ellipse"]
old-location: gdi\ellipse.htm
tech.root: gdi
ms.assetid: 9bec59dd-6bcb-498e-9ed2-ac641ecd7fa5
ms.date: 12/05/2018
ms.keywords: Ellipse, Ellipse function [Windows GDI], _win32_Ellipse, gdi.ellipse, wingdi/Ellipse
f1_keywords:
- wingdi/Ellipse
dev_langs:
- c++
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
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32Full.dll
api_name:
- Ellipse
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Ellipse function


## -description


The <b>Ellipse</b> function draws an ellipse. The center of the ellipse is the center of the specified bounding rectangle. The ellipse is outlined by using the current pen and is filled by using the current brush.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param left [in]

The x-coordinate, in logical coordinates, of the upper-left corner of the bounding rectangle.


### -param top [in]

The y-coordinate, in logical coordinates, of the upper-left corner of the bounding rectangle.


### -param right [in]

The x-coordinate, in logical coordinates, of the lower-right corner of the bounding rectangle.


### -param bottom [in]

The y-coordinate, in logical coordinates, of the lower-right corner of the bounding rectangle.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The current position is neither used nor updated by <b>Ellipse</b>.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/gdi/using-filled-shapes">Using Filled Shapes</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-arc">Arc
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-arcto">ArcTo
      </a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/filled-shape-functions">Filled Shape Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/filled-shapes">Filled Shapes Overview</a>
 

 

