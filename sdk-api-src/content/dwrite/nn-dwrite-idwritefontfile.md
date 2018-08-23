---
UID: NN:dwrite.IDWriteFontFile
title: IDWriteFontFile
author: windows-sdk-content
description: Represents a font file. Applications such as font managers or font viewers can call IDWriteFontFile::Analyze to find out if a particular file is a font file, and whether it is a font type that is supported by the font system.
old-location: directwrite\IDWriteFontFile.htm
old-project: DirectWrite
ms.assetid: d4be5466-0b6c-4cc5-9f16-aa00c6037eb9
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDWriteFontFile, IDWriteFontFile interface [Direct Write], IDWriteFontFile interface [Direct Write],described, directwrite.IDWriteFontFile, dwrite/IDWriteFontFile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dwrite.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFile
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteFontFile interface


## -description


 Represents a font file. Applications  such as font managers or font viewers can call <a href="https://msdn.microsoft.com/71acbcf8-3024-4e04-ac8e-89cf026b9e91">IDWriteFontFile::Analyze</a> to find out if a particular file is a font file, and whether it is a font type that is supported by the font system.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontFile</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteFontFile</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFontFile</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71acbcf8-3024-4e04-ac8e-89cf026b9e91">Analyze</a>
</td>
<td align="left" width="63%">
 Analyzes a file and returns whether it represents a font, and whether the font type is supported by the font system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60f13a03-2063-4f74-8bfe-217b6c1682ff">GetLoader</a>
</td>
<td align="left" width="63%">
 Obtains the file loader associated with a font file object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f76f0a0-2b4a-4983-88b9-0f1f2b7a7027">GetReferenceKey</a>
</td>
<td align="left" width="63%">
 Obtains the pointer to the reference key of a font file. The returned pointer is valid until the font file object is released. 

</td>
</tr>
</table> 

