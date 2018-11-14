---
UID: NN:dwrite_3.IDWriteTextLayout3
title: IDWriteTextLayout3
author: windows-sdk-content
description: Represents a block of text after it has been fully analyzed and formatted.
old-location: directwrite\idwritetextlayout3.htm
tech.root: DirectWrite
ms.assetid: a7741740-9524-caf0-650b-56808abcf328
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IDWriteTextLayout3, IDWriteTextLayout3 interface [Direct Write], IDWriteTextLayout3 interface [Direct Write],described, directwrite.idwritetextlayout3, dwrite_3/IDWriteTextLayout3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
---

# IDWriteTextLayout3 interface


## -description


Represents a block of text after it has been fully analyzed and formatted.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextLayout3</b> interface inherits from <a href="https://msdn.microsoft.com/034D795B-016A-401E-AD75-D5B0D1E87806">IDWriteTextLayout2</a>. <b>IDWriteTextLayout3</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/352ca3e3-7b08-823c-0881-0b051d4ce574">GetLineMetrics</a>
</td>
<td align="left" width="63%">
Retrieves properties of each line.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b93a3ec-c8ea-2e64-45b5-51565d6de173">GetLineSpacing</a>
</td>
<td align="left" width="63%">
Gets line spacing information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65b42ee1-5b67-1f6d-0e4b-ee60b192e7b7">InvalidateLayout</a>
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
<a href="https://msdn.microsoft.com/1bfca257-189c-4d18-628c-aff8217d2775">SetLineSpacing</a>
</td>
<td align="left" width="63%">
Set line spacing.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/034D795B-016A-401E-AD75-D5B0D1E87806">IDWriteTextLayout2</a>
 

 

