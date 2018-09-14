---
UID: NN:dwrite.IDWriteFontFileEnumerator
title: IDWriteFontFileEnumerator
author: windows-sdk-content
description: Encapsulates a collection of font files. The font system uses this interface to enumerate font files when building a font collection.
old-location: directwrite\IDWriteFontFileEnumerator.htm
tech.root: DirectWrite
ms.assetid: d89efffd-ccda-4d55-8419-de142b0f9652
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IDWriteFontFileEnumerator, IDWriteFontFileEnumerator interface [Direct Write], IDWriteFontFileEnumerator interface [Direct Write],described, directwrite.IDWriteFontFileEnumerator, dwrite/IDWriteFontFileEnumerator
ms.prod: windows
ms.technology: windows-sdk
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
 - IDWriteFontFileEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFileEnumerator interface


## -description


 Encapsulates a collection of font files. The font system uses this interface to enumerate font files when building a font collection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontFileEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteFontFileEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFontFileEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e541ab2b-2dc8-45df-9d72-8d55141ef142">GetCurrentFontFile</a>
</td>
<td align="left" width="63%">
 Gets a reference to the current font file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ffacdf0b-2e37-4b69-a6b5-7c6552ecdb60">MoveNext</a>
</td>
<td align="left" width="63%">
 Advances to the next font file in the collection. When it is first created, the enumerator is positioned
     before the first element of the collection and the first call to <b>MoveNext</b> advances to the first file.

</td>
</tr>
</table> 

