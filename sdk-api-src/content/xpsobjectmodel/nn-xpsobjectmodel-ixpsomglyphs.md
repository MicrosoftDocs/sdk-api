---
UID: NN:xpsobjectmodel.IXpsOMGlyphs
title: IXpsOMGlyphs
author: windows-sdk-content
description: Describes the text that appears on a page.
old-location: xps\ixpsomglyphs.htm
old-project: printdocs
ms.assetid: 6d2cda65-c719-46f2-97c9-8aee7b5f84b9
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IXpsOMGlyphs, IXpsOMGlyphs interface [XPS Documents and Packaging], IXpsOMGlyphs interface [XPS Documents and Packaging],described, xps.ixpsomglyphs, xpsobjectmodel/IXpsOMGlyphs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
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
 - IXpsOMGlyphs
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGlyphs interface


## -description


Describes the text that appears on a page.

The <a href="https://msdn.microsoft.com/5bdf2892-ce6f-4560-b638-e441166fc309">IXpsOMGlyphsEditor</a> interface is used to modify the text that is described by this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMGlyphs</b> interface inherits from <a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>. <b>IXpsOMGlyphs</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMGlyphs</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17110bb7-1ae9-41ef-aed1-8f1c00569825">GetBidiLevel</a>
</td>
<td align="left" width="63%">
Gets the level of bidirectional text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb288d73-da4d-4b46-95e5-c451c9ee2dc7">GetDeviceFontName</a>
</td>
<td align="left" width="63%">
Gets the name of the  device font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0deadd8e-24c5-4be1-8eaf-43cd59e22243">GetFillBrush</a>
</td>
<td align="left" width="63%">

              Gets a pointer to  the resolved <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a> interface of the fill brush to be used for the text.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d497eac9-8096-4a0e-bb43-315f734fd36e">GetFillBrushLocal</a>
</td>
<td align="left" width="63%">

              Gets a pointer to the  local, unshared <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a> interface of  the fill brush to be used for the text.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f71b0b98-12d6-4108-8b1e-4ad254ffbdfd">GetFillBrushLookup</a>
</td>
<td align="left" width="63%">

              Gets the lookup key of the <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a> interface that is stored in a resource dictionary and will be used as the fill brush.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/375e6391-c75f-4dbe-b51f-ce394f5088ec">GetFontFaceIndex</a>
</td>
<td align="left" width="63%">
Gets the index of the font face to be used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be1c6eff-20ef-49d3-929e-3595b421bcb9">GetFontRenderingEmSize</a>
</td>
<td align="left" width="63%">
Gets the font size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ecca6a0-eb47-4511-898d-cf097a78d6f0">GetFontResource</a>
</td>
<td align="left" width="63%">

              Gets a pointer to the  <a href="https://msdn.microsoft.com/dd0ce1c0-1c04-46a8-9075-93de9b3e3062">IXpsOMFontResource</a> interface of the font resource object required for this text.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae37e602-4a47-4234-a8d7-c757f3498308">GetGlyphIndexCount</a>
</td>
<td align="left" width="63%">
Gets the number of Glyph indices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6698ae0b-3525-4612-8234-8ba4dd2870a0">GetGlyphIndices</a>
</td>
<td align="left" width="63%">

              Gets an array of <a href="https://msdn.microsoft.com/0ea30e0f-f32b-4a38-9591-27cb1fe7f234">XPS_GLYPH_INDEX</a> structures that describe the specific glyph indices in the font.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c580aaf-72ed-4eff-b26e-8438d64f29e2">GetGlyphMappingCount</a>
</td>
<td align="left" width="63%">
Gets the number of glyph mappings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7cf4352-f08a-43cb-a063-5d369017a887">GetGlyphMappings</a>
</td>
<td align="left" width="63%">

              Gets an array of <a href="https://msdn.microsoft.com/5cc76cba-66e4-4853-969b-a99ec7bb22f3">XPS_GLYPH_MAPPING</a> structures that describe how to map UTF-16 scalar values to entries in the array of <a href="https://msdn.microsoft.com/0ea30e0f-f32b-4a38-9591-27cb1fe7f234">XPS_GLYPH_INDEX</a> structures, which is returned by <a href="https://msdn.microsoft.com/6698ae0b-3525-4612-8234-8ba4dd2870a0">GetGlyphIndices</a>.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c641d99-9303-484d-82e0-2d71e2c43561">GetGlyphsEditor</a>
</td>
<td align="left" width="63%">

              Gets a pointer to the <a href="https://msdn.microsoft.com/5bdf2892-ce6f-4560-b638-e441166fc309">IXpsOMGlyphsEditor</a> interface that will be used to edit the glyphs in the object.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51a0c84b-6f66-4bd5-b64c-b43ef4af8462">GetIsSideways</a>
</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the text is to be rendered with the glyphs rotated sideways.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec661cff-4671-401b-9c77-5036549762af">GetOrigin</a>
</td>
<td align="left" width="63%">
Gets the starting position of the text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f4974e9-b88b-40c0-89f5-b69fec5c2d83">GetProhibitedCaretStopCount</a>
</td>
<td align="left" width="63%">
Gets the number of prohibited caret stops.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e5372af-5233-4278-8b84-c3a308cc3041">GetProhibitedCaretStops</a>
</td>
<td align="left" width="63%">
Gets an array of prohibited caret stop locations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5678f67e-ed26-4846-b2f7-4e7f9690ca43">GetStyleSimulations</a>
</td>
<td align="left" width="63%">
Gets the style simulations that will  be applied when rendering the glyphs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b1573b5-c9c7-4c7b-8511-c5c2fc42ed3e">GetUnicodeString</a>
</td>
<td align="left" width="63%">
Gets the text in unescaped UTF-16 scalar values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73d1b0c2-81f9-4b1e-85fa-22e1e1c221f3">SetFillBrushLocal</a>
</td>
<td align="left" width="63%">

              Sets the <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a> interface pointer to a local, unshared fill brush.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a983583b-8698-48aa-af24-2e71d87d30c4">SetFillBrushLookup</a>
</td>
<td align="left" width="63%">
Sets the lookup key name of a shared fill brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9430474d-b874-47c7-b916-089280da8873">SetFontFaceIndex</a>
</td>
<td align="left" width="63%">
Sets the index of the font face to be used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9863caa0-9f43-45f7-9bed-c5b7187491de">SetFontRenderingEmSize</a>
</td>
<td align="left" width="63%">
Sets the font size of the text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0de80249-a1e1-4205-81bd-3ecb6cc938d4">SetFontResource</a>
</td>
<td align="left" width="63%">

              Sets the pointer to the  <a href="https://msdn.microsoft.com/dd0ce1c0-1c04-46a8-9075-93de9b3e3062">IXpsOMFontResource</a> interface of the font resource object that is required for this text.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5491bf0-bc40-491e-bf5e-f3fb580e10b4">SetOrigin</a>
</td>
<td align="left" width="63%">
Sets the starting position of the text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b87f12c-5d9b-47ea-99f0-e457c3e49c92">SetStyleSimulations</a>
</td>
<td align="left" width="63%">
Sets the style simulations that will be applied when the glyphs are rendered.

</td>
</tr>
</table> 


## -remarks



The code example that follows illustrates how to create an instance of  this interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
IXpsOMGlyphs       *newInterface;
// this interface is defined outside of this example
//  IXpsOMFontResource *font; 

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
    __uuidof(XpsOMObjectFactory),
    NULL,
    CLSCTX_INPROC_SERVER,
    _uuidof(IXpsOMObjectFactory),
    reinterpret_cast&lt;LPVOID*&gt;(&amp;xpsFactory)
    );

if (SUCCEEDED(hr))
{
    hr = xpsFactory-&gt;CreateGlyphs (font, &amp;newInterface);
    if (SUCCEEDED(hr))
    {
        // use newInterface

        newInterface-&gt;Release();
    }
    xpsFactory-&gt;Release();
}
else
{
    // evaluate HRESULT error returned in hr
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a>



<a href="https://msdn.microsoft.com/dd0ce1c0-1c04-46a8-9075-93de9b3e3062">IXpsOMFontResource</a>



<a href="https://msdn.microsoft.com/5bdf2892-ce6f-4560-b638-e441166fc309">IXpsOMGlyphsEditor</a>



<a href="https://msdn.microsoft.com/b97005dc-a79b-4234-b1a9-8fe705aea518">IXpsOMObjectFactory::CreateGlyphs</a>



<a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

