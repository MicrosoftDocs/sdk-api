---
UID: NN:dwrite_1.IDWriteFont1
title: IDWriteFont1 (dwrite_1.h)
author: windows-sdk-content
description: Represents a physical font in a font collection.
old-location: directwrite\idwritefont1.htm
tech.root: DirectWrite
ms.assetid: 50165292-8C5F-4FD2-A16B-9B8D9DB72F98
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteFont1, IDWriteFont1 interface [Direct Write], IDWriteFont1 interface [Direct Write],described, directwrite.idwritefont1, dwrite_1/IDWriteFont1
ms.topic: interface
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IDWriteFont1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFont1 interface


## -description


Represents a physical font in a font collection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFont1</b> interface inherits from <a href="https://msdn.microsoft.com/e29e626f-3e63-4c27-934b-64be51dcf3db">IDWriteFont</a>. <b>IDWriteFont1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFont1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2D8D22B9-3F5B-4257-8D74-699C4040C9DB">GetMetrics</a>
</td>
<td align="left" width="63%">
 Obtains design units and common metrics for the font face.
     These metrics are applicable to all the glyphs within a font face and are used by applications for layout calculations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DD31C1D6-4CD2-4ED0-BF9F-CAF587C613E6">GetPanose</a>
</td>
<td align="left" width="63%">
Gets the PANOSE values from the font and is used for font selection and
    matching.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B92E8500-AF63-43F2-A581-688B2CFCF2BF">GetUnicodeRanges</a>
</td>
<td align="left" width="63%">
Retrieves the list of character ranges supported by a font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AB05586C-47C9-4F65-A7DF-C2A40FC33253">IsMonospacedFont</a>
</td>
<td align="left" width="63%">
Determines if the font is monospaced, that is, the characters are the
    same fixed-pitch width (non-proportional).

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e29e626f-3e63-4c27-934b-64be51dcf3db">IDWriteFont</a>
 

 

