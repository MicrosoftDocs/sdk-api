---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.GetGlyphIndices
title: IXpsOMGlyphsEditor::GetGlyphIndices
author: windows-sdk-content
description: Gets an array of XPS_GLYPH_INDEX structures that describe the specific glyph indices in the font.
old-location: xps\ixpsomglyphseditor_getglyphindices.htm
tech.root: printdocs
ms.assetid: c174a123-245e-4b6d-8fef-a70e57948a48
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetGlyphIndices, GetGlyphIndices method [XPS Documents and Packaging], GetGlyphIndices method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, IXpsOMGlyphsEditor interface [XPS Documents and Packaging],GetGlyphIndices method, IXpsOMGlyphsEditor.GetGlyphIndices, IXpsOMGlyphsEditor::GetGlyphIndices, xps.ixpsomglyphseditor_getglyphindices, xpsobjectmodel/IXpsOMGlyphsEditor::GetGlyphIndices
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
 - IXpsOMGlyphsEditor.GetGlyphIndices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMGlyphsEditor::GetGlyphIndices


## -description


Gets an array of <a href="https://msdn.microsoft.com/en-us/library/Dd372958(v=VS.85).aspx">XPS_GLYPH_INDEX</a> structures that describe the specific glyph indices in the font.


## -parameters




### -param indexCount [in, out]

The number of elements that will fit in the array referenced by the <i>glyphIndices</i> parameter. When the method returns, <i>indexCount</i> will contain the number of <a href="https://msdn.microsoft.com/en-us/library/Dd372958(v=VS.85).aspx">XPS_GLYPH_INDEX</a> structures that are returned in the array referenced by <i>glyphIndices</i>.


### -param glyphIndices [out]

The <a href="https://msdn.microsoft.com/en-us/library/Dd372958(v=VS.85).aspx">XPS_GLYPH_INDEX</a> structure array that receives the glyph indices.


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
<i>indexCount</i> or <i>glyphIndices</i> is <b>NULL</b>, or both are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
<i>glyphIndices</i> is not large enough to receive the glyph index data. <i>indexCount</i> contains the required number of elements.

</td>
</tr>
</table>
 




## -remarks



 The glyph indices that are returned in <i>glyphIndices</i> override the default cmap mapping from the <b>UnicodeString</b> property to the glyph index. Each <a href="https://msdn.microsoft.com/en-us/library/Dd372958(v=VS.85).aspx">XPS_GLYPH_INDEX</a> structure also contains advance width and vertical and horizontal offset information.


<a href="https://msdn.microsoft.com/e7b83f08-e87f-4921-8dbb-f33453c63732">GetGlyphIndexCount</a> gets the number of elements in the glyph index array.




## -see-also




<a href="https://msdn.microsoft.com/5bdf2892-ce6f-4560-b638-e441166fc309">IXpsOMGlyphsEditor</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd372958(v=VS.85).aspx">XPS_GLYPH_INDEX</a>
 

 

