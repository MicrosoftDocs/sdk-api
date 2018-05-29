---
UID: NS:wingdi.tagEMRGRADIENTFILL
title: tagEMRGRADIENTFILL
author: windows-sdk-content
description: The EMRGRADIENTFILL structure contains members for the GradientFill enhanced metafile record.
old-location: gdi\emrgradientfill.htm
old-project: gdi
ms.assetid: efd12e71-ee26-4fc8-8e9f-5b0105ebe057
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: "*PEMRGRADIENTFILL, EMRGRADIENTFILL, EMRGRADIENTFILL structure [Windows GDI], GRADIENT_FILL_RECT_H, GRADIENT_FILL_RECT_V, GRADIENT_FILL_TRIANGLE, PEMRGRADIENTFILL, PEMRGRADIENTFILL structure pointer [Windows GDI], _win32_EMRGRADIENTFILL_str, gdi.emrgradientfill, tagEMRGRADIENTFILL, wingdi/EMRGRADIENTFILL, wingdi/PEMRGRADIENTFILL"
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: EMRGRADIENTFILL, *PEMRGRADIENTFILL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wingdi.h
api_name:
-	EMRGRADIENTFILL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagEMRGRADIENTFILL structure


## -description



The <b>EMRGRADIENTFILL</b> structure contains members for the <a href="https://msdn.microsoft.com/2f3e23e4-0105-4dcf-89ea-702ec2cf9e21">GradientFill</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field rclBounds

The bounding rectangle, in device units.


### -field nVer

The number of vertices.


### -field nTri

The number of rectangles or triangles to be passed to <a href="https://msdn.microsoft.com/2f3e23e4-0105-4dcf-89ea-702ec2cf9e21">GradientFill</a>.


### -field ulMode

The gradient fill mode. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GRADIENT_FILL_RECT_H"></a><a id="gradient_fill_rect_h"></a><dl>
<dt><b>GRADIENT_FILL_RECT_H</b></dt>
</dl>
</td>
<td width="60%">
In this mode, two endpoints describe a rectangle. The rectangle is defined to have a constant color (specified by the <a href="https://msdn.microsoft.com/47b700aa-3410-4610-ba06-dab2b2662f5e">TRIVERTEX</a> structure) for the left and right edges. GDI interpolates the color from the left to right edge and fills the interior.

</td>
</tr>
<tr>
<td width="40%"><a id="GRADIENT_FILL_RECT_V"></a><a id="gradient_fill_rect_v"></a><dl>
<dt><b>GRADIENT_FILL_RECT_V</b></dt>
</dl>
</td>
<td width="60%">
In this mode, two endpoints describe a rectangle. The rectangle is defined to have a constant color (specified by the <a href="https://msdn.microsoft.com/47b700aa-3410-4610-ba06-dab2b2662f5e">TRIVERTEX</a> structure) for the top and bottom edges. GDI interpolates the color from the top to bottom edge and fills the interior.

</td>
</tr>
<tr>
<td width="40%"><a id="GRADIENT_FILL_TRIANGLE"></a><a id="gradient_fill_triangle"></a><dl>
<dt><b>GRADIENT_FILL_TRIANGLE</b></dt>
</dl>
</td>
<td width="60%">
In this mode, an array of <a href="https://msdn.microsoft.com/47b700aa-3410-4610-ba06-dab2b2662f5e">TRIVERTEX</a> structures is passed to GDI along with a list of array indexes that describe separate triangles. GDI performs linear interpolation between triangle vertices and fills the interior. Drawing is done directly in 24- and 32-bpp modes. Dithering is performed in 16-, 8-, 4-, and 1-bpp mode.

</td>
</tr>
</table>
 


### -field Ver

An array of <a href="https://msdn.microsoft.com/47b700aa-3410-4610-ba06-dab2b2662f5e">TRIVERTEX</a> structures that each define a vertex.


## -remarks



This is a variable-length structure. The <b>Ver</b> member designates the beginning of the variable-length area. First comes an array of <b>nVer</b> <a href="https://msdn.microsoft.com/47b700aa-3410-4610-ba06-dab2b2662f5e">TRIVERTEX</a> structures to pass the vertices. Next comes an array of either <b>nTri</b> <a href="https://msdn.microsoft.com/71f3a4bd-5823-47ae-aa7a-f3058f18c591">GRADIENT_TRIANGLE</a> structures or <b>nTri</b> <a href="https://msdn.microsoft.com/8660114a-423f-40a8-b113-e0304bb0f383">GRADIENT_RECT</a> structures, depending on the value of <b>ulMode</b> (triangles or rectangles).

This structure is to be used during metafile playback.




## -see-also




<a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a>



<a href="https://msdn.microsoft.com/06582047-b64b-44ec-ae27-1f8ed7c56b97">EMR</a>



<a href="https://msdn.microsoft.com/8660114a-423f-40a8-b113-e0304bb0f383">GRADIENT_RECT</a>



<a href="https://msdn.microsoft.com/71f3a4bd-5823-47ae-aa7a-f3058f18c591">GRADIENT_TRIANGLE</a>



<a href="https://msdn.microsoft.com/2f3e23e4-0105-4dcf-89ea-702ec2cf9e21">GradientFill</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



Metafiles



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

