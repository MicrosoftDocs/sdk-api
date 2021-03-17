---
UID: NF:msctf.ITfCandidateListUIElement.GetPageIndex
title: ITfCandidateListUIElement::GetPageIndex (msctf.h)
description: The ITfCandidateListUIElement::GetPageIndex method returns the page index of the list.
helpviewer_keywords: ["GetPageIndex","GetPageIndex method [Text Services Framework]","GetPageIndex method [Text Services Framework]","ITfCandidateListUIElement interface","ITfCandidateListUIElement interface [Text Services Framework]","GetPageIndex method","ITfCandidateListUIElement.GetPageIndex","ITfCandidateListUIElement::GetPageIndex","msctf/ITfCandidateListUIElement::GetPageIndex","tsf.itfcandidatelistuielement_getpageindex"]
old-location: tsf\itfcandidatelistuielement_getpageindex.htm
tech.root: TSF
ms.assetid: d63afb41-0276-4bc9-af4d-319d39de519d
ms.date: 12/05/2018
ms.keywords: GetPageIndex, GetPageIndex method [Text Services Framework], GetPageIndex method [Text Services Framework],ITfCandidateListUIElement interface, ITfCandidateListUIElement interface [Text Services Framework],GetPageIndex method, ITfCandidateListUIElement.GetPageIndex, ITfCandidateListUIElement::GetPageIndex, msctf/ITfCandidateListUIElement::GetPageIndex, tsf.itfcandidatelistuielement_getpageindex
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
 - ITfCandidateListUIElement::GetPageIndex
 - msctf/ITfCandidateListUIElement::GetPageIndex
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
 - ITfCandidateListUIElement.GetPageIndex
---

# ITfCandidateListUIElement::GetPageIndex


## -description

The <b>ITfCandidateListUIElement::GetPageIndex</b> method returns the page index of the list.

## -parameters

### -param pIndex [out]

[out] A pointer that receives an array of the indexes that each page starts from. This can be <b>NULL</b>. The caller calls this method with <b>NULL</b> for this parameter first to get the number of pages in <i>puPageCnt</i> and allocates the buffer to receive indexes for all pages.

### -param uSize [in]

[in] A buffer size of <i>pIndex</i>.

### -param puPageCnt [out]

[out] A pointer to receive the page count.

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

