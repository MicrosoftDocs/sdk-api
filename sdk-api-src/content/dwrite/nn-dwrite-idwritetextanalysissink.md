---
UID: NN:dwrite.IDWriteTextAnalysisSink
title: IDWriteTextAnalysisSink
author: windows-sdk-content
description: This interface is implemented by the text analyzer's client to receive the output of a given text analysis.
old-location: directwrite\idwritetextanalysissink.htm
tech.root: DirectWrite
ms.assetid: 1fd2ca46-006c-4b01-8258-6c24f4be1641
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IDWriteTextAnalysisSink, IDWriteTextAnalysisSink interface [Direct Write], IDWriteTextAnalysisSink interface [Direct Write],described, directwrite.idwritetextanalysissink, dwrite/IDWriteTextAnalysisSink
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDWriteTextAnalysisSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextAnalysisSink interface


## -description


This interface is implemented by the text analyzer's client to receive the
 output of a given text analysis. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextAnalysisSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteTextAnalysisSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteTextAnalysisSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f51bae22-b4a0-4f72-a341-4479d66cfec5">SetBidiLevel</a>
</td>
<td align="left" width="63%">
Sets a bidirectional level on the range, which is  called once per  run change (either explicit or resolved implicit).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/423f1f0e-b2bd-48b6-aa3b-c79a2b542d5d">SetLineBreakpoints</a>
</td>
<td align="left" width="63%">
Sets line-break opportunities for each character, starting from the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09b00b49-702e-4cef-bf1c-397c5d572513">SetNumberSubstitution</a>
</td>
<td align="left" width="63%">
Sets the number substitution on the text range affected by the text analysis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/beae0420-b244-4c87-a3cb-a1b34562c3ed">SetScriptAnalysis</a>
</td>
<td align="left" width="63%">
Reports script analysis for the specified text range.

</td>
</tr>
</table> 


## -remarks



The text analyzer disregards any current
 state of the analysis sink, therefore, a Set method call on a range overwrites the previously set analysis result of the same range.



