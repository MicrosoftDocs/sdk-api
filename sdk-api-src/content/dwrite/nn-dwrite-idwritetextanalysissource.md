---
UID: NN:dwrite.IDWriteTextAnalysisSource
title: IDWriteTextAnalysisSource
author: windows-sdk-content
description: Implemented by the text analyzer's client to provide text to the analyzer.
old-location: directwrite\idwritetextanalysissource.htm
tech.root: DirectWrite
ms.assetid: 7e2a523d-9191-4f99-9e73-a7955c432126
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IDWriteTextAnalysisSource, IDWriteTextAnalysisSource interface [Direct Write], IDWriteTextAnalysisSource interface [Direct Write],described, directwrite.idwritetextanalysissource, dwrite/IDWriteTextAnalysisSource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextAnalysisSource interface


## -description


Implemented by the text analyzer's client to provide text to the analyzer. It allows the separation between the logical view of text as a continuous stream of characters identifiable by unique text positions, and the actual memory layout of potentially discrete blocks of text in the client's backing store. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextAnalysisSource</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteTextAnalysisSource</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/88a2474b-c14d-41ce-9687-f498644c0315">GetLocaleName</a>
</td>
<td align="left" width="63%">
Gets the locale name on the range affected by the text analysis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23e1539c-a58e-4123-82da-2f9d94309b05">GetNumberSubstitution</a>
</td>
<td align="left" width="63%">
Gets the number substitution from the text range affected by the text analysis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23013354-54bd-4f45-91d7-159965f0c56c">GetParagraphReadingDirection</a>
</td>
<td align="left" width="63%">
Gets the paragraph reading direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9deabfb-fd0b-4760-a148-b440587654d2">GetTextAtPosition</a>
</td>
<td align="left" width="63%">
Gets a block of text starting at the specified text position.
     

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af09985b-5f05-47da-be32-cc591fa58765">GetTextBeforePosition</a>
</td>
<td align="left" width="63%">
Gets a block of text immediately preceding the specified position.

</td>
</tr>
</table> 


## -remarks



If any of these callbacks returns an error, then the analysis functions will stop prematurely and return a callback error. Note that rather than return E_NOTIMPL,
 an application should stub the method and return a constant/null and S_OK.



