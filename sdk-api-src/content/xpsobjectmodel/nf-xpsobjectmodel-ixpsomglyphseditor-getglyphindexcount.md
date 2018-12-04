---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.GetGlyphIndexCount
title: IXpsOMGlyphsEditor::GetGlyphIndexCount
author: windows-sdk-content
description: Gets the number of glyph indices.
old-location: xps\ixpsomglyphseditor_getglyphindexcount.htm
tech.root: printdocs
ms.assetid: e7b83f08-e87f-4921-8dbb-f33453c63732
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetGlyphIndexCount, GetGlyphIndexCount method [XPS Documents and Packaging], GetGlyphIndexCount method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, IXpsOMGlyphsEditor interface [XPS Documents and Packaging],GetGlyphIndexCount method, IXpsOMGlyphsEditor.GetGlyphIndexCount, IXpsOMGlyphsEditor::GetGlyphIndexCount, xps.ixpsomglyphseditor_getglyphindexcount, xpsobjectmodel/IXpsOMGlyphsEditor::GetGlyphIndexCount
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IXpsOMGlyphsEditor.GetGlyphIndexCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMGlyphsEditor::GetGlyphIndexCount


## -description


Gets the number of glyph indices.


## -parameters




### -param indexCount [out, retval]

The glyph index count.


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
<i>indexCount</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



To get the glyph indices, call <a href="https://msdn.microsoft.com/c174a123-245e-4b6d-8fef-a70e57948a48">GetGlyphIndices</a>.




## -see-also




<a href="https://msdn.microsoft.com/5bdf2892-ce6f-4560-b638-e441166fc309">IXpsOMGlyphsEditor</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

