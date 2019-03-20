---
UID: NF:wingdi.EqualRgn
title: EqualRgn function (wingdi.h)
author: windows-sdk-content
description: The EqualRgn function checks the two specified regions to determine whether they are identical. The function considers two regions identical if they are equal in size and shape.
old-location: gdi\equalrgn.htm
tech.root: gdi
ms.assetid: c7829998-78f4-4334-bf34-92aad12555f5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EqualRgn, EqualRgn function [Windows GDI], _win32_EqualRgn, gdi.equalrgn, wingdi/EqualRgn
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
 - EqualRgn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EqualRgn function


## -description


The <b>EqualRgn</b> function checks the two specified regions to determine whether they are identical. The function considers two regions identical if they are equal in size and shape.


## -parameters




### -param hrgn1 [in]

Handle to a region.


### -param hrgn2 [in]

Handle to a region.


## -returns



If the two regions are equal, the return value is nonzero.

If the two regions are not equal, the return value is zero. A return value of ERROR means at least one of the region handles is invalid.




## -see-also




<a href="https://msdn.microsoft.com/17456440-c655-48ab-8d1e-ee770330f164">CreateRectRgn</a>



<a href="https://msdn.microsoft.com/f32e0b94-ce9c-4098-81fe-b239a9544621">CreateRectRgnIndirect</a>



<a href="https://msdn.microsoft.com/3a42fc7a-4c07-4540-99a7-520f99532f33">Region Functions</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>
 

 

