---
UID: NN:dwrite_2.IDWriteColorGlyphRunEnumerator
title: IDWriteColorGlyphRunEnumerator
author: windows-sdk-content
description: This interface allows the application to enumerate through the color glyph runs.
old-location: directwrite\idwritecolorglyphrunenumerator.htm
tech.root: DirectWrite
ms.assetid: 649AD648-32BB-4BF4-A82F-075E93505E33
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDWriteColorGlyphRunEnumerator, IDWriteColorGlyphRunEnumerator interface [Direct Write], IDWriteColorGlyphRunEnumerator interface [Direct Write],described, directwrite.idwritecolorglyphrunenumerator, dwrite_2/IDWriteColorGlyphRunEnumerator
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - IDWriteColorGlyphRunEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteColorGlyphRunEnumerator interface


## -description


This interface allows the application to enumerate through the color glyph runs. The enumerator enumerates the layers in a back to front order for appropriate layering.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteColorGlyphRunEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteColorGlyphRunEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteColorGlyphRunEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F4D89E35-3846-41F0-A724-3648DC9D487E">GetCurrentRun</a>
</td>
<td align="left" width="63%">
Returns the current glyph run of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E6336C0E-F880-485C-9111-A102298257C1">MoveNext</a>
</td>
<td align="left" width="63%">
Move to the next glyph run in the enumerator.

</td>
</tr>
</table> 

