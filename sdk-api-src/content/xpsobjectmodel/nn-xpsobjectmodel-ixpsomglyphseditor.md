---
UID: NN:xpsobjectmodel.IXpsOMGlyphsEditor
title: IXpsOMGlyphsEditor (xpsobjectmodel.h)
description: Allows batch modification of properties that affect the text content in an IXpsOMGlyphs interface.
helpviewer_keywords: ["IXpsOMGlyphsEditor","IXpsOMGlyphsEditor interface [XPS Documents and Packaging]","IXpsOMGlyphsEditor interface [XPS Documents and Packaging]","described","xps.ixpsomglyphseditor","xpsobjectmodel/IXpsOMGlyphsEditor"]
old-location: xps\ixpsomglyphseditor.htm
tech.root: xps
ms.assetid: 5bdf2892-ce6f-4560-b638-e441166fc309
ms.date: 12/05/2018
ms.keywords: IXpsOMGlyphsEditor, IXpsOMGlyphsEditor interface [XPS Documents and Packaging], IXpsOMGlyphsEditor interface [XPS Documents and Packaging],described, xps.ixpsomglyphseditor, xpsobjectmodel/IXpsOMGlyphsEditor
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
 - IXpsOMGlyphsEditor
 - xpsobjectmodel/IXpsOMGlyphsEditor
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
 - IXpsOMGlyphsEditor
---

# IXpsOMGlyphsEditor interface


## -description

Allows batch modification of properties that affect the text content in an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a> interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMGlyphsEditor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsOMGlyphsEditor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMGlyphsEditor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphseditor-applyedits">ApplyEdits</a>
</td>
<td align="left" width="63%">
Performs cross-property validation and then copies the changes to the parent <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphseditor-getbidilevel">GetBidiLevel</a>
</td>
<td align="left" width="63%">
Gets the bidirectional text level  of the parent  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphseditor-getdevicefontname">GetDeviceFontName</a>
</td>
<td align="left" width="63%">
Gets the name of the  device font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphseditor-getglyphindexcount">GetGlyphIndexCount</a>
</td>
<td align="left" width="63%">
Gets the number of glyph indices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphseditor-getglyphindices">GetGlyphIndices</a>
</td>
<td align="left" width="63%">
Gets an array of <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_index">XPS_GLYPH_INDEX</a> structures that describe the specific glyph indices in the font.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphseditor-getglyphmappingcount">GetGlyphMappingCount</a>
</td>
<td align="left" width="63%">
Gets the number of glyph mappings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphseditor-getglyphmappings">GetGlyphMappings</a>
</td>
<td align="left" width="63%">
Gets an array of <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_mapping">XPS_GLYPH_MAPPING</a> structures that describe how to map UTF-16 scalar values to entries in the array of <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_index">XPS_GLYPH_INDEX</a> structures, which is returned by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-getglyphindices">GetGlyphIndices</a>.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphseditor-getissideways">GetIsSideways</a>
</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the text is to be rendered with the glyphs rotated sideways.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphseditor-getprohibitedcaretstopcount">GetProhibitedCaretStopCount</a>
</td>
<td align="left" width="63%">
Gets the number of prohibited caret stops.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphseditor-getprohibitedcaretstops">GetProhibitedCaretStops</a>
</td>
<td align="left" width="63%">
Gets an array of prohibited caret stop locations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphseditor-getunicodestring">GetUnicodeString</a>
</td>
<td align="left" width="63%">
Gets the text in unescaped UTF-16 scalar values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphseditor-setbidilevel">SetBidiLevel</a>
</td>
<td align="left" width="63%">
Sets the level of bidirectional text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphseditor-setdevicefontname">SetDeviceFontName</a>
</td>
<td align="left" width="63%">
Sets the name of the device font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphseditor-setglyphindices">SetGlyphIndices</a>
</td>
<td align="left" width="63%">
Sets an <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_index">XPS_GLYPH_INDEX</a> structure array that describes which glyph indices are  to be used in the font.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphseditor-setglyphmappings">SetGlyphMappings</a>
</td>
<td align="left" width="63%">
Sets an array of <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_mapping">XPS_GLYPH_MAPPING</a> structures that describe how to map the UTF-16 scalar values in the <b>UnicodeString</b> property to entries in the array of <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_index">XPS_GLYPH_INDEX</a> structures.

            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphseditor-setissideways">SetIsSideways</a>
</td>
<td align="left" width="63%">
Sets the value that indicates whether the text is to be rendered with the glyphs rotated sideways.

            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphseditor-setprohibitedcaretstops">SetProhibitedCaretStops</a>
</td>
<td align="left" width="63%">
Sets an array of prohibited caret stop locations.

            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphseditor-setunicodestring">SetUnicodeString</a>
</td>
<td align="left" width="63%">
Sets the text in unescaped UTF-16 scalar values.

            

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-getglyphseditor">IXpsOMGlyphs::GetGlyphsEditor</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>