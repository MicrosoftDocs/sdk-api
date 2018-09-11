---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.SetBidiLevel
title: IXpsOMGlyphsEditor::SetBidiLevel
author: windows-sdk-content
description: Sets the level of bidirectional text.
old-location: xps\ixpsomglyphseditor_setbidilevel.htm
tech.root: printdocs
ms.assetid: a8035863-d1ed-4215-add3-6e60cfca7f1c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXpsOMGlyphsEditor interface [XPS Documents and Packaging],SetBidiLevel method, IXpsOMGlyphsEditor.SetBidiLevel, IXpsOMGlyphsEditor::SetBidiLevel, SetBidiLevel, SetBidiLevel method [XPS Documents and Packaging], SetBidiLevel method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, xps.ixpsomglyphseditor_setbidilevel, xpsobjectmodel/IXpsOMGlyphsEditor::SetBidiLevel
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
 - IXpsOMGlyphsEditor.SetBidiLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMGlyphsEditor::SetBidiLevel


## -description


Sets the level of bidirectional text.


## -parameters




### -param bidiLevel [in]

The level of bidirectional text.

Range: 0–61


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
The value of <i>bidiLevel</i> is outside of the allowed range. For more information, see the Remarks section.

</td>
</tr>
</table>
 




## -remarks



The <b>BidiLevel</b> property specifies the bidirectional nesting level of the Unicode algorithm. Even values imply the left-to-right layout and odd values the right-to-left layout. Right-to-left layout places the run origin on the right side of the first glyph. Advance widths  that are positive will move to the left, allowing subsequent glyphs to be placed to the left of the previous glyph.

The range of allowed values for this property is between 0 and 61, inclusive, and the default value is 0.




## -see-also




<a href="https://msdn.microsoft.com/5bdf2892-ce6f-4560-b638-e441166fc309">IXpsOMGlyphsEditor</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

