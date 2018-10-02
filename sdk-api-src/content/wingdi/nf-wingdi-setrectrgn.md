---
UID: NF:wingdi.SetRectRgn
title: SetRectRgn function
author: windows-sdk-content
description: The SetRectRgn function converts a region into a rectangular region with the specified coordinates.
old-location: gdi\setrectrgn.htm
tech.root: gdi
ms.assetid: 9a024d61-f397-43d8-a48e-edb8102a6f55
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SetRectRgn, SetRectRgn function [Windows GDI], _win32_SetRectRgn, gdi.setrectrgn, wingdi/SetRectRgn
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
 - Ext-MS-Win-RTCore-GDI-rgn-l1-1-0.dll
 - api-ms-win-gdi-ie-rgn-l1-1-0.dll
 - ie_shims.dll
 - ext-ms-win-rtcore-gdi-rgn-l1-1-1.dll
api_name:
 - SetRectRgn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetRectRgn function


## -description


The <b>SetRectRgn</b> function converts a region into a rectangular region with the specified coordinates.


## -parameters




### -param hrgn [in]

Handle to the region.


### -param left [in]

Specifies the x-coordinate of the upper-left corner of the rectangular region in logical units.


### -param top [in]

Specifies the y-coordinate of the upper-left corner of the rectangular region in logical units.


### -param right [in]

Specifies the x-coordinate of the lower-right corner of the rectangular region in logical units.


### -param bottom [in]

Specifies the y-coordinate of the lower-right corner of the rectangular region in logical units.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The region does not include the lower and right boundaries of the rectangle.




## -see-also




<a href="https://msdn.microsoft.com/17456440-c655-48ab-8d1e-ee770330f164">CreateRectRgn</a>



<a href="https://msdn.microsoft.com/3a42fc7a-4c07-4540-99a7-520f99532f33">Region Functions</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>
 

 

