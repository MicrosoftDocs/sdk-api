---
UID: NN:dwrite_3.IDWriteStringList
title: IDWriteStringList
author: windows-sdk-content
description: Represents a collection of strings indexed by number.
old-location: directwrite\idwritestringlist.htm
tech.root: DirectWrite
ms.assetid: 07A61B37-C63D-4F7D-888C-96B56F30F477
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDWriteStringList, IDWriteStringList interface [Direct Write], IDWriteStringList interface [Direct Write],described, directwrite.idwritestringlist, dwrite_3/IDWriteStringList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - IDWriteStringList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteStringList interface


## -description


Represents a collection of strings indexed by number.An IDWriteStringList is identical to IDWriteLocalizedStrings except for the semantics, where localized strings are indexed on language 
        (each language has one string property) whereas IDWriteStringList may contain multiple strings of the same language, such as a string list of family names from a
        font set. You can QueryInterface from an IDWriteLocalizedStrings to an IDWriteStringList.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteStringList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteStringList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteStringList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn958422(v=VS.85).aspx">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of strings in the string list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn958423(v=VS.85).aspx">GetLocaleName</a>
</td>
<td align="left" width="63%">
Copies the locale name with the specified index to the specified array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn958424(v=VS.85).aspx">GetLocaleNameLength</a>
</td>
<td align="left" width="63%">
Gets the length in characters (not including the null terminator) of the locale name with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn958425(v=VS.85).aspx">GetString</a>
</td>
<td align="left" width="63%">
Copies the string with the specified index to the specified array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn958426(v=VS.85).aspx">GetStringLength</a>
</td>
<td align="left" width="63%">
Gets the length in characters (not including the null terminator) of the string with the specified index.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

