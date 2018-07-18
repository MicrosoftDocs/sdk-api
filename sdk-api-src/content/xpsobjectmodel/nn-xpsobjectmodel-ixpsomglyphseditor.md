---
UID: NN:xpsobjectmodel.IXpsOMGlyphsEditor
title: IXpsOMGlyphsEditor
author: windows-sdk-content
description: Allows batch modification of properties that affect the text content in an IXpsOMGlyphs interface.
old-location: xps\ixpsomglyphseditor.htm
old-project: printdocs
ms.assetid: 5bdf2892-ce6f-4560-b638-e441166fc309
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IXpsOMGlyphsEditor, IXpsOMGlyphsEditor interface [XPS Documents and Packaging], IXpsOMGlyphsEditor interface [XPS Documents and Packaging],described, xps.ixpsomglyphseditor, xpsobjectmodel/IXpsOMGlyphsEditor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IXpsOMGlyphsEditor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGlyphsEditor interface


## -description


Allows batch modification of properties that affect the text content in an <a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMGlyphsEditor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsOMGlyphsEditor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ddbd8dc4-5d4f-4b30-8943-f4a5bc8e64c2">ApplyEdits</a>
</td>
<td align="left" width="63%">

              Performs cross-property validation and then copies the changes to the parent <a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86021e6e-5a91-44f5-814d-602705b97fb2">GetBidiLevel</a>
</td>
<td align="left" width="63%">

              Gets the bidirectional text level  of the parent  <a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79d1c913-0ed9-47bc-a06c-566a0ec19760">GetDeviceFontName</a>
</td>
<td align="left" width="63%">
Gets the name of the  device font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7b83f08-e87f-4921-8dbb-f33453c63732">GetGlyphIndexCount</a>
</td>
<td align="left" width="63%">
Gets the number of glyph indices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c174a123-245e-4b6d-8fef-a70e57948a48">GetGlyphIndices</a>
</td>
<td align="left" width="63%">

              Gets an array of <a href="https://msdn.microsoft.com/0ea30e0f-f32b-4a38-9591-27cb1fe7f234">XPS_GLYPH_INDEX</a> structures that describe the specific glyph indices in the font.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06aa2546-c1d1-47d6-9d3d-94d13310e42b">GetGlyphMappingCount</a>
</td>
<td align="left" width="63%">
Gets the number of glyph mappings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59a09a1f-547c-48e1-8aad-f408dd416656">GetGlyphMappings</a>
</td>
<td align="left" width="63%">

              Gets an array of <a href="https://msdn.microsoft.com/5cc76cba-66e4-4853-969b-a99ec7bb22f3">XPS_GLYPH_MAPPING</a> structures that describe how to map UTF-16 scalar values to entries in the array of <a href="https://msdn.microsoft.com/0ea30e0f-f32b-4a38-9591-27cb1fe7f234">XPS_GLYPH_INDEX</a> structures, which is returned by <a href="https://msdn.microsoft.com/6698ae0b-3525-4612-8234-8ba4dd2870a0">GetGlyphIndices</a>.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d115dbce-a81c-458f-8929-9e49e84a575d">GetIsSideways</a>
</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the text is to be rendered with the glyphs rotated sideways.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8aeb4868-f52e-4e80-b0c6-c8f759066fb2">GetProhibitedCaretStopCount</a>
</td>
<td align="left" width="63%">
Gets the number of prohibited caret stops.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/274d2137-c26f-438c-8c1b-591fbcb72c72">GetProhibitedCaretStops</a>
</td>
<td align="left" width="63%">
Gets an array of prohibited caret stop locations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48190202-2ab4-44ad-98e0-a69e9b48576f">GetUnicodeString</a>
</td>
<td align="left" width="63%">
Gets the text in unescaped UTF-16 scalar values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8035863-d1ed-4215-add3-6e60cfca7f1c">SetBidiLevel</a>
</td>
<td align="left" width="63%">
Sets the level of bidirectional text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d580f768-0c6a-4799-8ad8-d6f73b9216b9">SetDeviceFontName</a>
</td>
<td align="left" width="63%">
Sets the name of the device font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a95aaf48-9a55-4a62-b8e1-7b8d077f1b2e">SetGlyphIndices</a>
</td>
<td align="left" width="63%">

              Sets an <a href="https://msdn.microsoft.com/0ea30e0f-f32b-4a38-9591-27cb1fe7f234">XPS_GLYPH_INDEX</a> structure array that describes which glyph indices are  to be used in the font.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c09db1ca-b244-46bd-b01a-a40d260562eb">SetGlyphMappings</a>
</td>
<td align="left" width="63%">

              Sets an array of <a href="https://msdn.microsoft.com/5cc76cba-66e4-4853-969b-a99ec7bb22f3">XPS_GLYPH_MAPPING</a> structures that describe how to map the UTF-16 scalar values in the <b>UnicodeString</b> property to entries in the array of <a href="https://msdn.microsoft.com/0ea30e0f-f32b-4a38-9591-27cb1fe7f234">XPS_GLYPH_INDEX</a> structures.

            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67866971-fe2b-4354-a7e9-a43678443790">SetIsSideways</a>
</td>
<td align="left" width="63%">

              Sets the value that indicates whether the text is to be rendered with the glyphs rotated sideways.

            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f2e1014-d50b-4755-a533-239b6ba9009e">SetProhibitedCaretStops</a>
</td>
<td align="left" width="63%">

              Sets an array of prohibited caret stop locations.

            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68d5ab7d-63e4-403d-a689-6fc0a10e007c">SetUnicodeString</a>
</td>
<td align="left" width="63%">

              Sets the text in unescaped UTF-16 scalar values.

            

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a>



<a href="https://msdn.microsoft.com/1c641d99-9303-484d-82e0-2d71e2c43561">IXpsOMGlyphs::GetGlyphsEditor</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

