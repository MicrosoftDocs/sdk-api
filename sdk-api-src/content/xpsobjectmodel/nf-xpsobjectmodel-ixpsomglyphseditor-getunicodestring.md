---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.GetUnicodeString
title: IXpsOMGlyphsEditor::GetUnicodeString (xpsobjectmodel.h)
description: Gets the text in unescaped UTF-16 scalar values.
helpviewer_keywords: ["GetUnicodeString","GetUnicodeString method [XPS Documents and Packaging]","GetUnicodeString method [XPS Documents and Packaging]","IXpsOMGlyphsEditor interface","IXpsOMGlyphsEditor interface [XPS Documents and Packaging]","GetUnicodeString method","IXpsOMGlyphsEditor.GetUnicodeString","IXpsOMGlyphsEditor::GetUnicodeString","xps.ixpsomglyphseditor_getunicodestring","xpsobjectmodel/IXpsOMGlyphsEditor::GetUnicodeString"]
old-location: xps\ixpsomglyphseditor_getunicodestring.htm
tech.root: xps
ms.assetid: 48190202-2ab4-44ad-98e0-a69e9b48576f
ms.date: 12/05/2018
ms.keywords: GetUnicodeString, GetUnicodeString method [XPS Documents and Packaging], GetUnicodeString method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, IXpsOMGlyphsEditor interface [XPS Documents and Packaging],GetUnicodeString method, IXpsOMGlyphsEditor.GetUnicodeString, IXpsOMGlyphsEditor::GetUnicodeString, xps.ixpsomglyphseditor_getunicodestring, xpsobjectmodel/IXpsOMGlyphsEditor::GetUnicodeString
f1_keywords:
- xpsobjectmodel/IXpsOMGlyphsEditor.GetUnicodeString
dev_langs:
- c++
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
- IXpsOMGlyphsEditor.GetUnicodeString
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMGlyphsEditor::GetUnicodeString


## -description


Gets the text in unescaped UTF-16 scalar values.


## -parameters




### -param unicodeString [out, retval]

The UTF-16 Unicode string. If the string is empty, a <b>NULL</b> pointer is returned.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
<i>unicodeString</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method allocates the memory used by the string that is returned in <i>unicodeString</i>.  If <i>unicodeString</i> is not <b>NULL</b>, use the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor">IXpsOMGlyphsEditor</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 

