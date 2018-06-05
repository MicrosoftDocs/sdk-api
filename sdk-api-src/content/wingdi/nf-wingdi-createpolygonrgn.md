---
UID: NF:wingdi.CreatePolygonRgn
title: CreatePolygonRgn function
author: windows-sdk-content
description: The CreatePolygonRgn function creates a polygonal region.
old-location: gdi\createpolygonrgn.htm
old-project: gdi
ms.assetid: dd7ad6de-c5f2-46e4-8d28-24caaa48ba3a
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ALTERNATE, CreatePolygonRgn, CreatePolygonRgn function [Windows GDI], WINDING, _win32_CreatePolygonRgn, gdi.createpolygonrgn, wingdi/CreatePolygonRgn
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
-	Ext-MS-Win-RTCore-GDI-rgn-l1-1-0.dll
-	ext-ms-win-rtcore-gdi-rgn-l1-1-1.dll
api_name:
-	CreatePolygonRgn
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CreatePolygonRgn function


## -description


The <b>CreatePolygonRgn</b> function creates a polygonal region.


## -parameters




### -param pptl

TBD


### -param cPoint

TBD


### -param iMode

TBD




#### - cPoints [in]

The number of points in the array.


#### - fnPolyFillMode [in]

The fill mode used to determine which pixels are in the region. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ALTERNATE"></a><a id="alternate"></a><dl>
<dt><b>ALTERNATE</b></dt>
</dl>
</td>
<td width="60%">
Selects alternate mode (fills area between odd-numbered and even-numbered polygon sides on each scan line).

</td>
</tr>
<tr>
<td width="40%"><a id="WINDING"></a><a id="winding"></a><dl>
<dt><b>WINDING</b></dt>
</dl>
</td>
<td width="60%">
Selects winding mode (fills any region with a nonzero winding value).

</td>
</tr>
</table>
 

For more information about these modes, see the <a href="https://msdn.microsoft.com/233926c4-2658-405d-89b6-05ece844623d">SetPolyFillMode</a> function.


#### - lppt [in]

A pointer to an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structures that define the vertices of the polygon in logical units. The polygon is presumed closed. Each vertex can be specified only once.


## -returns



If the function succeeds, the return value is the handle to the region.

If the function fails, the return value is <b>NULL</b>.




## -remarks



When you no longer need the <b>HRGN</b> object, call the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete it.

Region coordinates are represented as 27-bit signed integers.

Regions created by the Create&lt;shape&gt;Rgn methods (such as <a href="https://msdn.microsoft.com/17456440-c655-48ab-8d1e-ee770330f164">CreateRectRgn</a> and <b>CreatePolygonRgn</b>) only include the interior of the shape; the shape's outline is excluded from the region. This means that any point on a line between two sequential vertices is not included in the region. If you were to call <a href="https://msdn.microsoft.com/6fab6126-4672-49d6-825b-66a7927a7e99">PtInRegion</a> for such a point, it would return zero as the result.




## -see-also




<a href="https://msdn.microsoft.com/1113d3dc-8e3f-436c-a5a8-191785bc7fcc">CreatePolyPolygonRgn</a>



<a href="https://msdn.microsoft.com/17456440-c655-48ab-8d1e-ee770330f164">CreateRectRgn</a>



<a href="https://msdn.microsoft.com/f32e0b94-ce9c-4098-81fe-b239a9544621">CreateRectRgnIndirect</a>



<a href="https://msdn.microsoft.com/16f387e1-b00c-4755-8b21-1ee0f25bc46b">
CreateRoundRectRgn</a>



<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">
DeleteObject</a>



<a href="https://msdn.microsoft.com/4dcff824-eb1d-425c-b246-db4ace2c6518">ExtCreateRegion</a>



<a href="https://msdn.microsoft.com/e0d4862d-a405-4c00-b7b0-af4dd60407c0">GetRegionData</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>



<a href="https://msdn.microsoft.com/3a42fc7a-4c07-4540-99a7-520f99532f33">
Region Functions</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">
Regions Overview</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">
SelectObject</a>



<a href="https://msdn.microsoft.com/233926c4-2658-405d-89b6-05ece844623d">SetPolyFillMode</a>
 

 

