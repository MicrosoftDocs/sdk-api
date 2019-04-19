---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.SetGlyphMappings
title: IXpsOMGlyphsEditor::SetGlyphMappings (xpsobjectmodel.h)
author: windows-sdk-content
description: Sets an array of XPS_GLYPH_MAPPING structures that describe how to map the UTF-16 scalar values in the UnicodeString property to entries in the array of XPS_GLYPH_INDEX structures.
old-location: xps\ixpsomglyphseditor_setglyphmappings.htm
tech.root: printdocs
ms.assetid: c09db1ca-b244-46bd-b01a-a40d260562eb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMGlyphsEditor interface [XPS Documents and Packaging],SetGlyphMappings method, IXpsOMGlyphsEditor.SetGlyphMappings, IXpsOMGlyphsEditor::SetGlyphMappings, SetGlyphMappings, SetGlyphMappings method [XPS Documents and Packaging], SetGlyphMappings method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, xps.ixpsomglyphseditor_setglyphmappings, xpsobjectmodel/IXpsOMGlyphsEditor::SetGlyphMappings
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMGlyphsEditor.SetGlyphMappings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMGlyphsEditor::SetGlyphMappings


## -description


Sets an array of <a href="https://msdn.microsoft.com/en-us/library/Dd372959(v=VS.85).aspx">XPS_GLYPH_MAPPING</a> structures that describe how to map the UTF-16 scalar values in the <b>UnicodeString</b> property to entries in the array of <a href="https://msdn.microsoft.com/en-us/library/Dd372958(v=VS.85).aspx">XPS_GLYPH_INDEX</a> structures.




## -parameters




### -param glyphMappingCount [in]

The number of <a href="https://msdn.microsoft.com/en-us/library/Dd372959(v=VS.85).aspx">XPS_GLYPH_MAPPING</a> structures in the array that is referenced by <i>glyphMappings</i>. A value of 0 clears the property.


### -param glyphMappings [in]

An  <a href="https://msdn.microsoft.com/en-us/library/Dd372959(v=VS.85).aspx">XPS_GLYPH_MAPPING</a> structure array that contains the glyph mapping values. If <i>glyphMappingCount</i> is 0, this parameter is ignored and can be set to <b>NULL</b>.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A member of one or more <a href="https://msdn.microsoft.com/en-us/library/Dd372959(v=VS.85).aspx">XPS_GLYPH_MAPPING</a> structures has a value that  is not valid. This can occur in the following cases: the sum of string length and start position is less than the start position; the sum of index position and index length is less than the start position; and length of indices is 0.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>glyphMappings</i> is <b>NULL</b> and <i>glyphMappingCount</i> is greater than 0.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_MAPPING_OUT_OF_ORDER</b></dt>
</dl>
</td>
<td width="60%">
In one or more <a href="https://msdn.microsoft.com/en-us/library/Dd372959(v=VS.85).aspx">XPS_GLYPH_MAPPING</a> structures, an element  is out of sequence.


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5bdf2892-ce6f-4560-b638-e441166fc309">IXpsOMGlyphsEditor</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd372959(v=VS.85).aspx">XPS_GLYPH_MAPPING</a>
 

 

