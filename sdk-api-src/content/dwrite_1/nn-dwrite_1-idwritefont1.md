---
UID: NN:dwrite_1.IDWriteFont1
title: IDWriteFont1 (dwrite_1.h)

description: Represents a physical font in a font collection.
old-location: directwrite\idwritefont1.htm
tech.root: DirectWrite
ms.assetid: 50165292-8C5F-4FD2-A16B-9B8D9DB72F98

ms.date: 12/05/2018
ms.keywords: IDWriteFont1, IDWriteFont1 interface [Direct Write], IDWriteFont1 interface [Direct Write],described, directwrite.idwritefont1, dwrite_1/IDWriteFont1
ms.topic: interface
f1_keywords: 
 - "dwrite_1/IDWriteFont1"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFont1 interface


## -description


Represents a physical font in a font collection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFont1</b> interface inherits from <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefont">IDWriteFont</a>. <b>IDWriteFont1</b> also has these types of members:
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
<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getmetrics">GetMetrics</a>
</td>
<td align="left" width="63%">
 Obtains design units and common metrics for the font face.
     These metrics are applicable to all the glyphs within a font face and are used by applications for layout calculations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose">GetPanose</a>
</td>
<td align="left" width="63%">
Gets the PANOSE values from the font and is used for font selection and
    matching.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getunicoderanges">GetUnicodeRanges</a>
</td>
<td align="left" width="63%">
Retrieves the list of character ranges supported by a font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-ismonospacedfont">IsMonospacedFont</a>
</td>
<td align="left" width="63%">
Determines if the font is monospaced, that is, the characters are the
    same fixed-pitch width (non-proportional).

</td>
</tr>
</table> 


## -see-also




<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefont">IDWriteFont</a>
 

 

