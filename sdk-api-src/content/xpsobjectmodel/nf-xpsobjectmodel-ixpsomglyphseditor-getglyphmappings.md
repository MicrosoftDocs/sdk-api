---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.GetGlyphMappings
title: IXpsOMGlyphsEditor::GetGlyphMappings
author: windows-sdk-content
description: Gets an array of XPS_GLYPH_MAPPING structures that describe how to map UTF-16 scalar values to entries in the array of XPS_GLYPH_INDEX structures, which is returned by GetGlyphIndices.
old-location: xps\ixpsomglyphseditor_getglyphmappings.htm
old-project: printdocs
ms.assetid: 59a09a1f-547c-48e1-8aad-f408dd416656
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetGlyphMappings, GetGlyphMappings method [XPS Documents and Packaging], GetGlyphMappings method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, IXpsOMGlyphsEditor interface [XPS Documents and Packaging],GetGlyphMappings method, IXpsOMGlyphsEditor.GetGlyphMappings, IXpsOMGlyphsEditor::GetGlyphMappings, xps.ixpsomglyphseditor_getglyphmappings, xpsobjectmodel/IXpsOMGlyphsEditor::GetGlyphMappings
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMGlyphsEditor.GetGlyphMappings
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGlyphsEditor::GetGlyphMappings


## -description


Gets an array of <a href="https://msdn.microsoft.com/5cc76cba-66e4-4853-969b-a99ec7bb22f3">XPS_GLYPH_MAPPING</a> structures that describe how to map UTF-16 scalar values to entries in the array of <a href="https://msdn.microsoft.com/0ea30e0f-f32b-4a38-9591-27cb1fe7f234">XPS_GLYPH_INDEX</a> structures, which is returned by <a href="https://msdn.microsoft.com/6698ae0b-3525-4612-8234-8ba4dd2870a0">GetGlyphIndices</a>.


## -parameters




### -param glyphMappingCount [in, out]

The number of <a href="https://msdn.microsoft.com/5cc76cba-66e4-4853-969b-a99ec7bb22f3">XPS_GLYPH_MAPPING</a> structures that will fit in the array referenced by  <i>glyphMappings</i>. When the method returns, <i>glyphMappingCount</i> will contain the number of values in that array.


### -param glyphMappings [out]

An array of <a href="https://msdn.microsoft.com/5cc76cba-66e4-4853-969b-a99ec7bb22f3">XPS_GLYPH_MAPPING</a> structures that receives the glyph mapping values.


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
<i>glyphMappingCount</i> or <i>glyphMappings</i> is <b>NULL</b>.

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




<a href="https://msdn.microsoft.com/06aa2546-c1d1-47d6-9d3d-94d13310e42b">GetGlyphMappingCount</a> gets the number of glyph mappings.




## -see-also




<a href="https://msdn.microsoft.com/c174a123-245e-4b6d-8fef-a70e57948a48">GetGlyphIndices</a>



<a href="https://msdn.microsoft.com/5bdf2892-ce6f-4560-b638-e441166fc309">IXpsOMGlyphsEditor</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/5cc76cba-66e4-4853-969b-a99ec7bb22f3">XPS_GLYPH_MAPPING</a>
 

 

