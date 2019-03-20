---
UID: NS:wingdi._TRIVERTEX
title: TRIVERTEX (wingdi.h)
author: windows-sdk-content
description: The TRIVERTEX structure contains color information and position information.
old-location: gdi\trivertex.htm
tech.root: gdi
ms.assetid: 47b700aa-3410-4610-ba06-dab2b2662f5e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPTRIVERTEX, *PTRIVERTEX, PTRIVERTEX, PTRIVERTEX structure pointer [Windows GDI], TRIVERTEX, TRIVERTEX structure [Windows GDI], _win32_TRIVERTEX_str, gdi.trivertex, wingdi/PTRIVERTEX, wingdi/TRIVERTEX"
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - TRIVERTEX
product: Windows
targetos: Windows
req.typenames: TRIVERTEX, *PTRIVERTEX, *LPTRIVERTEX
req.redist: 
---

# TRIVERTEX structure


## -description



The <b>TRIVERTEX</b> structure contains color information and position information.




## -struct-fields




### -field x

The x-coordinate, in logical units, of the upper-left corner of the rectangle.


### -field y

The y-coordinate, in logical units, of the upper-left corner of the rectangle.


### -field Red

The color information at the point of x, y.


### -field Green

The color information at the point of x, y.


### -field Blue

The color information at the point of x, y.


### -field Alpha

The color information at the point of x, y.


## -remarks



In the <b>TRIVERTEX</b> structure, x and y indicate position in the same manner as in the <a href="https://msdn.microsoft.com/587d36c8-e81c-4256-af25-af2a82727e8d">POINTL</a> structure contained in the wtypes.h header file. <b>Red</b>, <b>Green</b>, <b>Blue</b>, and <b>Alpha</b> members indicate color information at the point x, y. The color information of each channel is specified as a value from 0x0000 to 0xff00. This allows higher color resolution for an object that has been split into small triangles for display. The <b>TRIVERTEX</b> structure contains information needed by the <i>pVertex</i> parameter of <a href="https://msdn.microsoft.com/2f3e23e4-0105-4dcf-89ea-702ec2cf9e21">GradientFill</a>.


#### Examples

For an example of the use of this structure, see <a href="https://msdn.microsoft.com/78834f92-00cb-4899-851a-1de5e3c1f4fa">Drawing a Shaded Triangle</a> or <a href="https://msdn.microsoft.com/a4277e22-03f8-470f-87e9-5aeab258b6d2">Drawing a Shaded Rectangle</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/29f8237f-9c7e-41a7-90b1-5f048fcc74a6">Bitmap Structures</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/2f3e23e4-0105-4dcf-89ea-702ec2cf9e21">GradientFill</a>



<a href="https://msdn.microsoft.com/587d36c8-e81c-4256-af25-af2a82727e8d">POINTL</a>
 

 

