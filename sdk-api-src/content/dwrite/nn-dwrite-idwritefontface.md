---
UID: NN:dwrite.IDWriteFontFace
title: IDWriteFontFace
author: windows-sdk-content
description: Represents an absolute reference to a font face which contains font face type, appropriate file references, face identification data and various font data such as metrics, names and glyph outlines.
old-location: directwrite\IDWriteFontFace.htm
tech.root: DirectWrite
ms.assetid: 1b6bb9e2-cf01-413c-9ee8-42bb0f703ce8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDWriteFontFace, IDWriteFontFace interface [Direct Write], IDWriteFontFace interface [Direct Write],described, directwrite.IDWriteFontFace, dwrite/IDWriteFontFace
ms.topic: interface
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFace interface


## -description


Represents an absolute reference to a font face which contains font face type, appropriate file references,  face identification data and various font data such as metrics, names and glyph outlines. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontFace</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteFontFace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFontFace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4da03cbe-5287-4d9c-aaa2-cff3dbf259fc">GetDesignGlyphMetrics</a>
</td>
<td align="left" width="63%">
 Obtains ideal (resolution-independent) glyph metrics in font design units. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/505238e5-bfc9-4d5e-b807-3c5e8b2e82d3">GetFiles</a>
</td>
<td align="left" width="63%">
 Obtains the font files representing a font face.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7bda3916-6db3-4f56-b18c-288506c0b646">GetGdiCompatibleGlyphMetrics</a>
</td>
<td align="left" width="63%">
Obtains glyph metrics in font design units with the return values compatible with what GDI would produce.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e132ec0-64cb-4681-b079-02a0047badd5">GetGdiCompatibleMetrics</a>
</td>
<td align="left" width="63%">
Obtains design units and common metrics for the font face.
    These metrics are applicable to all the glyphs within a fontface and are used by applications for layout calculations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd030905-2c97-4d1b-9a77-eb7e52bcd901">GetGlyphCount</a>
</td>
<td align="left" width="63%">
 Obtains the number of glyphs in the font face.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2dbaec8c-464e-45a5-b420-fa1ec3d224bd">GetGlyphIndices</a>
</td>
<td align="left" width="63%">
 Returns the nominal mapping of UCS4 Unicode code points to glyph indices as defined by the font 'CMAP' table.
     

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06edbd68-efc3-44e5-875c-a84488fca252">GetGlyphRunOutline</a>
</td>
<td align="left" width="63%">
 Computes the outline of a run of glyphs by calling back to the outline sink interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69c87fcf-775c-4c6d-971c-e1bb999d246b">GetIndex</a>
</td>
<td align="left" width="63%">
 Obtains the index of a font face in the context of its font files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09271b06-71cb-4702-861f-c3f6b9069c15">GetMetrics</a>
</td>
<td align="left" width="63%">
 Obtains design units and common metrics for the font face.
     These metrics are applicable to all the glyphs within a font face and are used by applications for layout calculations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54504bcb-b05c-4b63-8704-8d718cf2ee16">GetRecommendedRenderingMode</a>
</td>
<td align="left" width="63%">
 Determines the recommended rendering mode for the font, using the specified size and rendering parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/409f5e6e-af3c-4d31-968c-d26a89aa1e9d">GetSimulations</a>
</td>
<td align="left" width="63%">
 Obtains the algorithmic style simulation flags of a font face.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ea4b0b0-faf4-4291-838d-480e2bc68b0c">GetType</a>
</td>
<td align="left" width="63%">
 Obtains the file format type of a font face.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c29a9806-8c6c-4b9a-a535-ed8f382cda31">IsSymbolFont</a>
</td>
<td align="left" width="63%">
 Determines whether the font is a symbol font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e9b7e30-eae9-476b-89bd-a794e08ba468">ReleaseFontTable</a>
</td>
<td align="left" width="63%">
 Releases the table obtained earlier from <a href="https://msdn.microsoft.com/82ce9078-0b50-4e8c-a38a-181ec71d6136">TryGetFontTable</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82ce9078-0b50-4e8c-a38a-181ec71d6136">TryGetFontTable</a>
</td>
<td align="left" width="63%">
 Finds the specified OpenType font table if it exists and returns a pointer to it.
     The function accesses the underlying font data through the <a href="https://msdn.microsoft.com/792ab9be-853f-427d-a762-2da8e81423f8">IDWriteFontFileStream</a> interface
     implemented by the font file loader.

</td>
</tr>
</table> 

