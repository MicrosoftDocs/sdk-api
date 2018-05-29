---
UID: NF:dwrite_3.AddFontFaceReference
title: AddFontFaceReference function
author: windows-sdk-content
description: Adds a reference to a font to the set being built.
old-location: directwrite\idwritefontsetbuilder_addfontfacereference_overload.htm
old-project: DirectWrite
ms.assetid: 2543720f-1b5a-ca1d-9e24-3fcd61a4de37
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: AddFontFaceReference, AddFontFaceReference methods [Direct Write], IDWriteFontSetBuilder::AddFontFaceReference, directwrite.idwritefontsetbuilder_addfontfacereference_overload, dwrite_3/AddFontFaceReference
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dwrite_3.h
api_name:
-	IDWriteFontSetBuilder::AddFontFaceReference
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# AddFontFaceReference function


## -description


<span>Adds a reference to a font to the set being built.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0E67F5EF-F8BB-47D9-995D-40879351DC17">AddFontFaceReference(IDWriteFontFaceReference*)</a>
</td>
<td align="left" width="63%">
Adds a reference to a font to the set being built. The necessary metadata will automatically be extracted from the font upon calling CreateFontSet.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4211E9FC-205D-4C2D-A8F3-612B841D490D">AddFontFaceReference(IDWriteFontFaceReference*, const DWRITE_FONT_PROPERTY*, UINT32)</a>
</td>
<td align="left" width="63%">
Adds a reference to a font to the set being built. The caller supplies enough information to search on, avoiding the need to open
          the potentially non-local font. Any properties not supplied by the caller will be missing, and those properties will not be available as
          filters in GetMatchingFonts. GetPropertyValues for missing properties will return an empty string list. The properties passed should generally
          be consistent with the actual font contents, but they need not be. You could, for example, alias a font using a different name or unique
          identifier, or you could set custom tags not present in the actual font.

</td>
</tr>
</table>

## -parameters


## -see-also




<a href="https://msdn.microsoft.com/CC6C95CA-BA8B-47C4-A241-650EC8477192">IDWriteFontSetBuilder</a>
 

 

