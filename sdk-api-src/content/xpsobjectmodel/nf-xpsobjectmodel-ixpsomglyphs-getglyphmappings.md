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

# IXpsOMGlyphs::GetGlyphMappings


## -description


Gets an array of <a href="https://msdn.microsoft.com/5cc76cba-66e4-4853-969b-a99ec7bb22f3">XPS_GLYPH_MAPPING</a> structures that describe how to map UTF-16 scalar values to entries in the array of <a href="https://msdn.microsoft.com/0ea30e0f-f32b-4a38-9591-27cb1fe7f234">XPS_GLYPH_INDEX</a> structures, which is returned by <a href="https://msdn.microsoft.com/6698ae0b-3525-4612-8234-8ba4dd2870a0">GetGlyphIndices</a>.


## -parameters




### -param glyphMappingCount [in, out]

The number of <a href="https://msdn.microsoft.com/5cc76cba-66e4-4853-969b-a99ec7bb22f3">XPS_GLYPH_MAPPING</a> structures that will fit in the array referenced by <i>glyphMappings</i>. When the method returns, <i>glyphMappingCount</i> contains the number of values returned in the array referenced by <i>glyphMappings</i>.


### -param glyphMappings [in, out]

An array of <a href="https://msdn.microsoft.com/5cc76cba-66e4-4853-969b-a99ec7bb22f3">XPS_GLYPH_MAPPING</a> structures that contain the glyph mapping values.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>glyphMappingCount</i>, <i>glyphMappings</i>, or both are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
<i>glyphMappings</i> is not large enough to receive the glyph index data. <i>glyphMappingCount</i> contains the required number of elements.

</td>
</tr>
</table>
 




## -remarks




<a href="https://msdn.microsoft.com/6c580aaf-72ed-4eff-b26e-8438d64f29e2">GetGlyphMappingCount</a> gets the number of glyph mappings.




## -see-also




<a href="https://msdn.microsoft.com/6c580aaf-72ed-4eff-b26e-8438d64f29e2">GetGlyphMappingCount</a>



<a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/0ea30e0f-f32b-4a38-9591-27cb1fe7f234">XPS_GLYPH_INDEX</a>



<a href="https://msdn.microsoft.com/5cc76cba-66e4-4853-969b-a99ec7bb22f3">XPS_GLYPH_MAPPING</a>
 

 

