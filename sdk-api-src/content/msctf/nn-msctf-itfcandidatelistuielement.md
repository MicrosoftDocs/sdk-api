---
UID: NN:msctf.ITfCandidateListUIElement
title: ITfCandidateListUIElement (msctf.h)
author: windows-sdk-content
description: The ITfCandidateListUIElement interface is implemented by a text service that has the candidate list UI.
old-location: tsf\itfcandidatelistuielement.htm
tech.root: TSF
ms.assetid: 1f39aa06-3c94-4959-b857-ca61498d5b5c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfCandidateListUIElement, ITfCandidateListUIElement interface [Text Services Framework], ITfCandidateListUIElement interface [Text Services Framework],described, _tsf_itfcandidatelistuielement_ref, msctf/ITfCandidateListUIElement, tsf.itfcandidatelistuielement
ms.topic: interface
f1_keywords: 
 - "msctf/ITfCandidateListUIElement"
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.h
api_name:
 - ITfCandidateListUIElement
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfCandidateListUIElement interface


## -description


The <b>ITfCandidateListUIElement</b> interface is implemented by a text service that has the candidate list UI.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfCandidateListUIElement</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfCandidateListUIElement</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfCandidateListUIElement</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcandidatelistuielement-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Returns the count of the candidate strings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcandidatelistuielement-getcurrentpage">GetCurrentPage</a>
</td>
<td align="left" width="63%">
Returns the current page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcandidatelistuielement-getdocumentmgr">GetDocumentMgr</a>
</td>
<td align="left" width="63%">
Returns the target document manager of this UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d63afb41-0276-4bc9-af4d-319d39de519d">GetPageIndex</a>
</td>
<td align="left" width="63%">
Returns the page index of the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcandidatelistuielement-getselection">GetSelection</a>
</td>
<td align="left" width="63%">
Returns the current selection of the candidate list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcandidatelistuielement-getstring">GetString</a>
</td>
<td align="left" width="63%">
Returns the string of the index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcandidatelistuielement-getupdatedflags">GetUpdatedFlags</a>
</td>
<td align="left" width="63%">
Returns the flag that tells which part of this element was updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcandidatelistuielement-setpageindex">SetPageIndex</a>
</td>
<td align="left" width="63%">
Set the page index.

</td>
</tr>
</table> 

