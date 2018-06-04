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

# GetPropertyValues function


## -description


<span>Returns property values for the font set.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7841266-9850-1ffd-c5f8-ef5c9b623ada">GetPropertyValues(DWRITE_FONT_PROPERTY_ID, IDWriteStringList**)</a>
</td>
<td align="left" width="63%">

          Returns all unique property values in the set, which can be used
          for purposes such as displaying a family list or tag cloud. All values
          are returned regardless of language, including all localized names.
        

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c99c3b76-8513-5700-0641-33284e5e2f21">GetPropertyValues(DWRITE_FONT_PROPERTY_ID, const WCHAR*, IDWriteStringList**)</a>
</td>
<td align="left" width="63%">

          Returns all unique property values in the set, which can be used
          for purposes such as displaying a family list or tag cloud. Values are
          returned in priority order according to the language list, such that if
          a font contains more than one localized name, the preferred one will be
          returned.
        

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4523d5a6-9d5f-61ac-a47f-810fef1522a9">GetPropertyValues(UINT32, DWRITE_FONT_PROPERTY_ID, BOOL*, IDWriteLocalizedStrings**)</a>
</td>
<td align="left" width="63%">
Returns the property values of a specific font item index.

</td>
</tr>
</table>

## -parameters


## -see-also




<a href="https://msdn.microsoft.com/0178f248-8dc0-c0ee-63c1-8db3f6ef94c3">IDWriteFontSet</a>
 

 

