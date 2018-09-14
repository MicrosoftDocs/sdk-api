---
UID: NN:dwrite.IDWriteLocalFontFileLoader
title: IDWriteLocalFontFileLoader
author: windows-sdk-content
description: A built-in implementation of the IDWriteFontFileLoader interface, that operates on local font files and exposes local font file information from the font file reference key.
old-location: directwrite\idwritelocalfontfileloader.htm
tech.root: DirectWrite
ms.assetid: acb777c8-24c6-452e-8f58-8fb2ad8c0b6c
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IDWriteLocalFontFileLoader, IDWriteLocalFontFileLoader interface [Direct Write], IDWriteLocalFontFileLoader interface [Direct Write],described, directwrite.idwritelocalfontfileloader, dwrite/IDWriteLocalFontFileLoader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dwrite.h
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
 - IDWriteLocalFontFileLoader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteLocalFontFileLoader interface


## -description


A built-in implementation of the <a href="https://msdn.microsoft.com/855e281e-3855-4c11-af87-68f8e0dadbf8">IDWriteFontFileLoader</a> interface, that operates on local font files
and exposes local font file information from the font file reference key. Font file references created using <a href="https://msdn.microsoft.com/ec67407d-e19b-4135-83ff-f3115e2da90c">CreateFontFileReference</a> use this font file loader.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteLocalFontFileLoader</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteLocalFontFileLoader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteLocalFontFileLoader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a61cfe80-100d-4813-b04f-a39f626893dd">GetFilePathFromKey</a>
</td>
<td align="left" width="63%">
Obtains the absolute font file path from the font file reference key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bdd84d75-5a7a-448a-a52c-0f5997ab07b9">GetFilePathLengthFromKey</a>
</td>
<td align="left" width="63%">
Obtains the length of the absolute file path from the font file reference key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce7f5321-8ad8-4412-a54c-7102790e99c0">GetLastWriteTimeFromKey</a>
</td>
<td align="left" width="63%">
Obtains the last write time of the file from the font file reference key.

</td>
</tr>
</table> 

