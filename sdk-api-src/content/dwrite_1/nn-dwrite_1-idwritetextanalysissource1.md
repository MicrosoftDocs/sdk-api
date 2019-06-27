---
UID: NN:dwrite_1.IDWriteTextAnalysisSource1
title: IDWriteTextAnalysisSource1 (dwrite_1.h)
author: windows-sdk-content
description: The interface you implement to provide needed information to the text analyzer, like the text and associated text properties.
old-location: directwrite\idwritetextanalysissource1.htm
tech.root: DirectWrite
ms.assetid: CFB9DB16-1F0B-409F-97BC-BB4B693AB3D6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteTextAnalysisSource1, IDWriteTextAnalysisSource1 interface [Direct Write], IDWriteTextAnalysisSource1 interface [Direct Write],described, directwrite.idwritetextanalysissource1, dwrite_1/IDWriteTextAnalysisSource1
ms.topic: interface
f1_keywords: 
 - "dwrite_1/IDWriteTextAnalysisSource1"
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
 - IDWriteTextAnalysisSource1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextAnalysisSource1 interface


## -description


The interface you implement to provide needed information to  the text analyzer, like the text and associated text properties.


<div class="alert"><b>Note</b>   If any of these callbacks return an error, the analysis functions will  stop prematurely and return a callback error.  </div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextAnalysisSource1</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritetextanalysissource">IDWriteTextAnalysisSource</a>. <b>IDWriteTextAnalysisSource1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteTextAnalysisSource1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_1/nf-dwrite_1-idwritetextanalysissource1-getverticalglyphorientation">GetVerticalGlyphOrientation</a>
</td>
<td align="left" width="63%">
Used by the text analyzer to obtain the desired glyph
    orientation and resolved bidi level.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritetextanalysissource">IDWriteTextAnalysisSource</a>
 

 

