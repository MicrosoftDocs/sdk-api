---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

