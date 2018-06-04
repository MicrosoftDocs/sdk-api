---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ComputeGlyphOrigins function


## -description


<span>Converts glyph run placements to glyph origins.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0AA609E2-28C3-4D0C-A627-0648FB0D126A">ComputeGlyphOrigins(DWRITE_GLYPH_RUN, DWRITE_MEASURING_MODE, D2D1_POINT_2F, DWRITE_MATRIX, D2D1_POINT_2F*)</a>
</td>
<td align="left" width="63%">
Converts glyph run placements to glyph origins.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7D086964-3659-428D-82E5-D14237BF7DFB">ComputeGlyphOrigins(DWRITE_GLYPH_RUN, D2D1_POINT_2F, D2D1_POINT_2F*)</a>
</td>
<td align="left" width="63%">
Converts glyph run placements to glyph origins. This overload is for natural metrics, which includes SVG, TrueType natural modes, and bitmap placement.

</td>
</tr>
</table>

## -parameters


## -see-also




<a href="https://msdn.microsoft.com/D3C5E48A-A062-430A-A196-CAC621F346FC">IDWriteFactory4</a>
 

 

