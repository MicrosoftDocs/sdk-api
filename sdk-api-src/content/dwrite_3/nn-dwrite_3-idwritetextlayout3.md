---
UID: NN:dwrite_3.IDWriteTextLayout3
title: IDWriteTextLayout3 (dwrite_3.h)
author: windows-sdk-content
description: Represents a block of text after it has been fully analyzed and formatted.
old-location: directwrite\idwritetextlayout3.htm
tech.root: DirectWrite
ms.assetid: a7741740-9524-caf0-650b-56808abcf328
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteTextLayout3, IDWriteTextLayout3 interface [Direct Write], IDWriteTextLayout3 interface [Direct Write],described, directwrite.idwritetextlayout3, dwrite_3/IDWriteTextLayout3
ms.topic: interface
f1_keywords: 
 - "dwrite_3/IDWriteTextLayout3"
req.header: dwrite_3.h
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
 - IDWriteTextLayout3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextLayout3 interface


## -description


Represents a block of text after it has been fully analyzed and formatted.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextLayout3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/DirectWrite/idwritetextlayout2">IDWriteTextLayout2</a>. <b>IDWriteTextLayout3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteTextLayout3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/DirectWrite/idwritetextlayout3-getlinemetrics">GetLineMetrics</a>
</td>
<td align="left" width="63%">
Retrieves properties of each line.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/DirectWrite/idwritetextlayout3-getlinespacing">GetLineSpacing</a>
</td>
<td align="left" width="63%">
Gets line spacing information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/DirectWrite/idwritetextlayout3-invalidatelayout">InvalidateLayout</a>
</td>
<td align="left" width="63%">
Invalidates the layout, forcing layout to remeasure before calling the   
   metrics or drawing functions. This is useful if the locality of a font    
   changes, and layout should be redrawn, or if the size of a client    
   implemented IDWriteInlineObject changes. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/DirectWrite/idwritetextlayout3-setlinespacing">SetLineSpacing</a>
</td>
<td align="left" width="63%">
Set line spacing.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectWrite/idwritetextlayout2">IDWriteTextLayout2</a>
 

 

