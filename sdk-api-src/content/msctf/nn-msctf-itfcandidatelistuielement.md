---
UID: NN:msctf.ITfCandidateListUIElement
title: ITfCandidateListUIElement
author: windows-sdk-content
description: The ITfCandidateListUIElement interface is implemented by a text service that has the candidate list UI.
old-location: tsf\itfcandidatelistuielement.htm
old-project: TSF
ms.assetid: 1f39aa06-3c94-4959-b857-ca61498d5b5c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfCandidateListUIElement, ITfCandidateListUIElement interface [Text Services Framework], ITfCandidateListUIElement interface [Text Services Framework],described, _tsf_itfcandidatelistuielement_ref, msctf/ITfCandidateListUIElement, tsf.itfcandidatelistuielement
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.redist: TSF 1.0 on Windows 2000 Professional
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
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
req.lib: 
req.dll: Imekrcic.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfCandidateListUIElement interface


## -description


The <b>ITfCandidateListUIElement</b> interface is implemented by a text service that has the candidate list UI.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfCandidateListUIElement</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfCandidateListUIElement</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/9009203a-71d1-49b2-823d-d6f04bf3743b">GetCount</a>
</td>
<td align="left" width="63%">
Returns the count of the candidate strings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/551c73ff-8fbd-47e5-a6e8-90d58141c7c0">GetCurrentPage</a>
</td>
<td align="left" width="63%">
Returns the current page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/def8e85d-8180-4ad4-9d70-07adef0ce5fb">GetDocumentMgr</a>
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
<a href="https://msdn.microsoft.com/ac7530cd-eac8-4b2b-89e1-e05c14a81c7d">GetSelection</a>
</td>
<td align="left" width="63%">
Returns the current selection of the candidate list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85cf60e3-f068-499f-b726-9ccea3cd8503">GetString</a>
</td>
<td align="left" width="63%">
Returns the string of the index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/618bf940-3145-4da5-a253-620b17b045c8">GetUpdatedFlags</a>
</td>
<td align="left" width="63%">
Returns the flag that tells which part of this element was updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e7a5185-2e4b-4f8e-b7c0-d9462d61b113">SetPageIndex</a>
</td>
<td align="left" width="63%">
Set the page index.

</td>
</tr>
</table> 

