---
UID: NF:wingdi.InvertRgn
title: InvertRgn function
author: windows-sdk-content
description: The InvertRgn function inverts the colors in the specified region.
old-location: gdi\invertrgn.htm
tech.root: gdi
ms.assetid: 94704c44-796a-4ca7-97f3-6676d7f94078
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: InvertRgn, InvertRgn function [Windows GDI], _win32_InvertRgn, gdi.invertrgn, wingdi/InvertRgn
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - InvertRgn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InvertRgn function


## -description


The <b>InvertRgn</b> function inverts the colors in the specified region.


## -parameters




### -param hdc [in]

Handle to the device context.


### -param hrgn [in]

Handle to the region for which colors are inverted. The region's coordinates are presumed to be logical coordinates.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



On monochrome screens, the <b>InvertRgn</b> function makes white pixels black and black pixels white. On color screens, this inversion is dependent on the type of technology used to generate the colors for the screen.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/64cd6e82-7a0d-4b5e-b491-450f37eea43a">Using Brushes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/c4e0eca5-442b-462b-a4f2-0c628b6d3d38">FillRgn</a>



<a href="https://msdn.microsoft.com/7656fb67-d865-459e-b379-4f2e44c76fd0">PaintRgn</a>



<a href="https://msdn.microsoft.com/3a42fc7a-4c07-4540-99a7-520f99532f33">Region Functions</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>
 

 

