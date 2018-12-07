---
UID: NN:dwrite_2.IDWriteTextLayout2
title: IDWriteTextLayout2
author: windows-sdk-content
description: Represents a block of text after it has been fully analyzed and formatted.
old-location: directwrite\idwritetextlayout2.htm
tech.root: DirectWrite
ms.assetid: 034D795B-016A-401E-AD75-D5B0D1E87806
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDWriteTextLayout2, IDWriteTextLayout2 interface [Direct Write], IDWriteTextLayout2 interface [Direct Write],described, directwrite.idwritetextlayout2, dwrite_2/IDWriteTextLayout2
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
 - IDWriteTextLayout2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextLayout2 interface


## -description


Represents a block of text after it has been fully analyzed and formatted.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextLayout2</b> interface inherits from <a href="https://msdn.microsoft.com/FF6B3C78-0CC0-4843-9D17-3CF0777EA8BA">IDWriteTextLayout1</a>. <b>IDWriteTextLayout2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteTextLayout2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65787E7E-7475-4810-B929-377D50A2BEF5">GetFontFallback</a>
</td>
<td align="left" width="63%">
Get the current font fallback object.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ACB83321-C193-41E6-84D8-493334E30885">GetLastLineWrapping</a>
</td>
<td align="left" width="63%">
Get whether or not the last word on the last line is wrapped.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EADCD83A-9FF5-44AB-8AB5-35FCB3A84889">GetMetrics</a>
</td>
<td align="left" width="63%">
 Retrieves overall metrics for the formatted string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C372B1F9-E874-48AE-B22E-72D883B6DBF9">GetOpticalAlignment</a>
</td>
<td align="left" width="63%">
Get how the glyphs align to the edges the margin.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A98AFAC5-77D7-4917-AE1D-85B2B450C043">GetVerticalGlyphOrientation</a>
</td>
<td align="left" width="63%">
Get the preferred orientation of glyphs when using a vertical reading direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63B86AE4-92D4-4748-A6E2-987B740080EB">SetFontFallback</a>
</td>
<td align="left" width="63%">
Apply a custom font fallback onto layout.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/424ADF2E-42DC-414B-8588-5A326CA4A507">SetLastLineWrapping</a>
</td>
<td align="left" width="63%">
Set whether or not the last word on the last line is wrapped. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10C9C3E7-4556-4848-A4CB-F822A689CAB0">SetOpticalAlignment</a>
</td>
<td align="left" width="63%">
Set how the glyphs align to the edges the margin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DB6A8163-0D64-4438-A51A-3CD0B8B0C64A">SetVerticalGlyphOrientation</a>
</td>
<td align="left" width="63%">
Set the preferred orientation of glyphs when using a vertical reading direction.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/FF6B3C78-0CC0-4843-9D17-3CF0777EA8BA">IDWriteTextLayout1</a>
 

 

