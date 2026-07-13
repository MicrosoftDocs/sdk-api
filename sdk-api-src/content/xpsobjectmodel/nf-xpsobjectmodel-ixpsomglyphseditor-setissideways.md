---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.SetIsSideways
title: IXpsOMGlyphsEditor::SetIsSideways (xpsobjectmodel.h)
description: Sets the value that indicates whether the text is to be rendered with the glyphs rotated sideways.
helpviewer_keywords: ["FALSE","IXpsOMGlyphsEditor interface [XPS Documents and Packaging]","SetIsSideways method","IXpsOMGlyphsEditor.SetIsSideways","IXpsOMGlyphsEditor::SetIsSideways","SetIsSideways","SetIsSideways method [XPS Documents and Packaging]","SetIsSideways method [XPS Documents and Packaging]","IXpsOMGlyphsEditor interface","TRUE","xps.ixpsomglyphseditor_setissideways","xpsobjectmodel/IXpsOMGlyphsEditor::SetIsSideways"]
old-location: xps\ixpsomglyphseditor_setissideways.htm
tech.root: xps
ms.assetid: 67866971-fe2b-4354-a7e9-a43678443790
ms.date: 12/05/2018
ms.keywords: FALSE, IXpsOMGlyphsEditor interface [XPS Documents and Packaging],SetIsSideways method, IXpsOMGlyphsEditor.SetIsSideways, IXpsOMGlyphsEditor::SetIsSideways, SetIsSideways, SetIsSideways method [XPS Documents and Packaging], SetIsSideways method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, TRUE, xps.ixpsomglyphseditor_setissideways, xpsobjectmodel/IXpsOMGlyphsEditor::SetIsSideways
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMGlyphsEditor::SetIsSideways
 - xpsobjectmodel/IXpsOMGlyphsEditor::SetIsSideways
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMGlyphsEditor.SetIsSideways
---

# IXpsOMGlyphsEditor::SetIsSideways


## -description

Sets the value that indicates whether the text is to be rendered with the glyphs rotated sideways.

## -parameters

### -param isSideways [in]

The Boolean value that indicates whether the text is to be rendered with the glyphs rotated sideways.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Rotate the glyphs sideways. Produces sideways text.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not rotate the glyphs sideways. Produces normal text.

</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor">IXpsOMGlyphsEditor</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>