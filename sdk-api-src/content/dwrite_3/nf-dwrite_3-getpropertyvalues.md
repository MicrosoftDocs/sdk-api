---
UID: NF:dwrite_3.GetPropertyValues
title: GetPropertyValues function
author: windows-sdk-content
description: Returns property values for the font set.
old-location: directwrite\idwritefontset_getpropertyvalues_overload.htm
old-project: DirectWrite
ms.assetid: 3c3fd5b7-88dd-d434-0b62-f365b407c379
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: GetPropertyValues, GetPropertyValues methods [Direct Write], IDWriteFontSet::GetPropertyValues, directwrite.idwritefontset_getpropertyvalues_overload, dwrite_3/GetPropertyValues
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
-	IDWriteFontSet::GetPropertyValues
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 

