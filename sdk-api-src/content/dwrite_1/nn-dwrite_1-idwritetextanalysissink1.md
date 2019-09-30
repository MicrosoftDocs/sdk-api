---
UID: NN:dwrite_1.IDWriteTextAnalysisSink1
title: IDWriteTextAnalysisSink1 (dwrite_1.h)
author: windows-sdk-content
description: The interface you implement to receive the output of the text analyzers.
old-location: directwrite\idwritetextanalysissink1.htm
tech.root: DirectWrite
ms.assetid: 46882D89-CD59-4C4F-A8BD-1ABC8B8C5C4B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteTextAnalysisSink1, IDWriteTextAnalysisSink1 interface [Direct Write], IDWriteTextAnalysisSink1 interface [Direct Write],described, directwrite.idwritetextanalysissink1, dwrite_1/IDWriteTextAnalysisSink1
ms.topic: interface
f1_keywords: 
 - "dwrite_1/IDWriteTextAnalysisSink1"
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
 - IDWriteTextAnalysisSink1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextAnalysisSink1 interface


## -description


 The interface you implement to receive the  output of the text analyzers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextAnalysisSink1</b> interface inherits from <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissink">IDWriteTextAnalysisSink</a>. <b>IDWriteTextAnalysisSink1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteTextAnalysisSink1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalysissink1-setglyphorientation">SetGlyphOrientation</a>
</td>
<td align="left" width="63%">
The text analyzer calls back to this to report the actual orientation
    of each character for shaping and drawing.

</td>
</tr>
</table> 


## -see-also




<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissink">IDWriteTextAnalysisSink</a>
 

 

