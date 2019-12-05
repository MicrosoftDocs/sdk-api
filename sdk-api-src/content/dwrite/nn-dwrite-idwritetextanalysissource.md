---
UID: NN:dwrite.IDWriteTextAnalysisSource
title: IDWriteTextAnalysisSource (dwrite.h)
description: Implemented by the text analyzer's client to provide text to the analyzer.
old-location: directwrite\idwritetextanalysissource.htm
tech.root: DirectWrite
ms.assetid: 7e2a523d-9191-4f99-9e73-a7955c432126
ms.date: 12/05/2018
ms.keywords: IDWriteTextAnalysisSource, IDWriteTextAnalysisSource interface [Direct Write], IDWriteTextAnalysisSource interface [Direct Write],described, directwrite.idwritetextanalysissource, dwrite/IDWriteTextAnalysisSource
ms.topic: interface
f1_keywords:
- dwrite/IDWriteTextAnalysisSource
dev_langs:
- c++
req.header: dwrite.h
req.include-header: 
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
- IDWriteTextAnalysisSource
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextAnalysisSource interface


## -description


Implemented by the text analyzer's client to provide text to the analyzer. It allows the separation between the logical view of text as a continuous stream of characters identifiable by unique text positions, and the actual memory layout of potentially discrete blocks of text in the client's backing store. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextAnalysisSource</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteTextAnalysisSource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteTextAnalysisSource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissource-getlocalename">GetLocaleName</a>
</td>
<td align="left" width="63%">
Gets the locale name on the range affected by the text analysis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissource-getnumbersubstitution">GetNumberSubstitution</a>
</td>
<td align="left" width="63%">
Gets the number substitution from the text range affected by the text analysis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissource-getparagraphreadingdirection">GetParagraphReadingDirection</a>
</td>
<td align="left" width="63%">
Gets the paragraph reading direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissource-gettextatposition">GetTextAtPosition</a>
</td>
<td align="left" width="63%">
Gets a block of text starting at the specified text position.
     

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissource-gettextbeforeposition">GetTextBeforePosition</a>
</td>
<td align="left" width="63%">
Gets a block of text immediately preceding the specified position.

</td>
</tr>
</table> 


## -remarks



If any of these callbacks returns an error, then the analysis functions will stop prematurely and return a callback error. Note that rather than return E_NOTIMPL,
 an application should stub the method and return a constant/null and S_OK.



