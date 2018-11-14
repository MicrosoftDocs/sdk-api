---
UID: NF:wingdi.GetRegionData
title: GetRegionData function
author: windows-sdk-content
description: The GetRegionData function fills the specified buffer with data describing a region. This data includes the dimensions of the rectangles that make up the region.
old-location: gdi\getregiondata.htm
tech.root: gdi
ms.assetid: e0d4862d-a405-4c00-b7b0-af4dd60407c0
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetRegionData, GetRegionData function [Windows GDI], _win32_GetRegionData, gdi.getregiondata, wingdi/GetRegionData
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
 - Ext-MS-Win-GDI-rgn-l1-1-0.dll
 - Ext-MS-Win-RTCore-GDI-rgn-l1-1-0.dll
 - api-ms-win-gdi-ie-rgn-l1-1-0.dll
 - ie_shims.dll
 - ext-ms-win-rtcore-gdi-rgn-l1-1-1.dll
 - GDI32Full.dll
api_name:
 - GetRegionData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetRegionData
: 
---

# GetRegionData function


## -description


The <b>GetRegionData</b> function fills the specified buffer with data describing a region. This data includes the dimensions of the rectangles that make up the region.


## -parameters




### -param hrgn [in]

A handle to the region.


### -param nCount [in]

The size, in bytes, of the <i>lpRgnData</i> buffer.


### -param lpRgnData [out]

A pointer to a <a href="https://msdn.microsoft.com/3eac0b23-3138-4b34-9c16-6cc185e4de22">RGNDATA</a> structure that receives the information. The dimensions of the region are in logical units. If this parameter is <b>NULL</b>, the return value contains the number of bytes needed for the region data.


## -returns



If the function succeeds and <i>dwCount</i> specifies an adequate number of bytes, the return value is always <i>dwCount</i>. If <i>dwCount</i> is too small or the function fails, the return value is 0. If <i>lpRgnData</i> is <b>NULL</b>, the return value is the required number of bytes.

If the function fails, the return value is zero.




## -remarks



The <b>GetRegionData</b> function is used in conjunction with the <a href="https://msdn.microsoft.com/4dcff824-eb1d-425c-b246-db4ace2c6518">ExtCreateRegion</a> function.




## -see-also




<a href="https://msdn.microsoft.com/1113d3dc-8e3f-436c-a5a8-191785bc7fcc">CreatePolyPolygonRgn</a>



<a href="https://msdn.microsoft.com/dd7ad6de-c5f2-46e4-8d28-24caaa48ba3a">CreatePolygonRgn</a>



<a href="https://msdn.microsoft.com/17456440-c655-48ab-8d1e-ee770330f164">CreateRectRgn</a>



<a href="https://msdn.microsoft.com/f32e0b94-ce9c-4098-81fe-b239a9544621">CreateRectRgnIndirect</a>



<a href="https://msdn.microsoft.com/16f387e1-b00c-4755-8b21-1ee0f25bc46b">CreateRoundRectRgn</a>



<a href="https://msdn.microsoft.com/4dcff824-eb1d-425c-b246-db4ace2c6518">ExtCreateRegion</a>



<a href="https://msdn.microsoft.com/3eac0b23-3138-4b34-9c16-6cc185e4de22">RGNDATA</a>



<a href="https://msdn.microsoft.com/3a42fc7a-4c07-4540-99a7-520f99532f33">Region Functions</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>
 

 

