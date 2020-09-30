---
UID: NF:msctf.ITfCandidateListUIElement.GetCurrentPage
title: ITfCandidateListUIElement::GetCurrentPage (msctf.h)
description: The ITfCandidateListUIElement::GetCurrentPage method returns the current page.
helpviewer_keywords: ["GetCurrentPage","GetCurrentPage method [Text Services Framework]","GetCurrentPage method [Text Services Framework]","ITfCandidateListUIElement interface","ITfCandidateListUIElement interface [Text Services Framework]","GetCurrentPage method","ITfCandidateListUIElement.GetCurrentPage","ITfCandidateListUIElement::GetCurrentPage","msctf/ITfCandidateListUIElement::GetCurrentPage","tsf.itfcandidatelistuielement_getcurrentpage"]
old-location: tsf\itfcandidatelistuielement_getcurrentpage.htm
tech.root: TSF
ms.assetid: 551c73ff-8fbd-47e5-a6e8-90d58141c7c0
ms.date: 12/05/2018
ms.keywords: GetCurrentPage, GetCurrentPage method [Text Services Framework], GetCurrentPage method [Text Services Framework],ITfCandidateListUIElement interface, ITfCandidateListUIElement interface [Text Services Framework],GetCurrentPage method, ITfCandidateListUIElement.GetCurrentPage, ITfCandidateListUIElement::GetCurrentPage, msctf/ITfCandidateListUIElement::GetCurrentPage, tsf.itfcandidatelistuielement_getcurrentpage
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
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfCandidateListUIElement::GetCurrentPage
 - msctf/ITfCandidateListUIElement::GetCurrentPage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfCandidateListUIElement.GetCurrentPage
---

# ITfCandidateListUIElement::GetCurrentPage


## -description

The <b>ITfCandidateListUIElement::GetCurrentPage</b> method returns the current page.

## -parameters

### -param puPage [in]

[in] A pointer to receive the current page index.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>

