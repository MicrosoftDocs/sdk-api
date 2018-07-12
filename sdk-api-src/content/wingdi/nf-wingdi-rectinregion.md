---
UID: NF:wingdi.RectInRegion
title: RectInRegion function
author: windows-sdk-content
description: The RectInRegion function determines whether any part of the specified rectangle is within the boundaries of a region.
old-location: gdi\rectinregion.htm
old-project: gdi
ms.assetid: 198a02f1-120c-4f65-aa7c-a41f2e5e81a9
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: RectInRegion, RectInRegion function [Windows GDI], _win32_RectInRegion, gdi.rectinregion, wingdi/RectInRegion
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
 - RectInRegion
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# RectInRegion function


## -description


The <b>RectInRegion</b> function determines whether any part of the specified rectangle is within the boundaries of a region.


## -parameters




### -param hrgn [in]

Handle to the region.


### -param lprect

TBD




#### - lprc [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure containing the coordinates of the rectangle in logical units. The lower and right edges of the rectangle are not included.


## -returns



If any part of the specified rectangle lies within the boundaries of the region, the return value is nonzero.

If no part of the specified rectangle lies within the boundaries of the region, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/6fab6126-4672-49d6-825b-66a7927a7e99">PtInRegion</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<a href="https://msdn.microsoft.com/3a42fc7a-4c07-4540-99a7-520f99532f33">Region Functions</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>
 

 

