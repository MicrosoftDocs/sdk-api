---
UID: NF:msctf.ITfCandidateListUIElement.GetDocumentMgr
title: ITfCandidateListUIElement::GetDocumentMgr (msctf.h)
description: The ITfCandidateListUIElement::GetDocumentMgr method returns the target document manager of this UI.
helpviewer_keywords: ["GetDocumentMgr","GetDocumentMgr method [Text Services Framework]","GetDocumentMgr method [Text Services Framework]","ITfCandidateListUIElement interface","ITfCandidateListUIElement interface [Text Services Framework]","GetDocumentMgr method","ITfCandidateListUIElement.GetDocumentMgr","ITfCandidateListUIElement::GetDocumentMgr","msctf/ITfCandidateListUIElement::GetDocumentMgr","tsf.itfcandidatelistuielement_getdocumentmgr"]
old-location: tsf\itfcandidatelistuielement_getdocumentmgr.htm
tech.root: TSF
ms.assetid: def8e85d-8180-4ad4-9d70-07adef0ce5fb
ms.date: 12/05/2018
ms.keywords: GetDocumentMgr, GetDocumentMgr method [Text Services Framework], GetDocumentMgr method [Text Services Framework],ITfCandidateListUIElement interface, ITfCandidateListUIElement interface [Text Services Framework],GetDocumentMgr method, ITfCandidateListUIElement.GetDocumentMgr, ITfCandidateListUIElement::GetDocumentMgr, msctf/ITfCandidateListUIElement::GetDocumentMgr, tsf.itfcandidatelistuielement_getdocumentmgr
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
 - ITfCandidateListUIElement::GetDocumentMgr
 - msctf/ITfCandidateListUIElement::GetDocumentMgr
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
 - ITfCandidateListUIElement.GetDocumentMgr
---

# ITfCandidateListUIElement::GetDocumentMgr


## -description

The <b>ITfCandidateListUIElement::GetDocumentMgr</b> method returns the target document manager of this UI.

## -parameters

### -param ppdim [out]

[out] A pointer to receive <a href="/windows/desktop/api/msctf/nn-msctf-itfdocumentmgr">ITfDocumentMgr</a> interface pointer.

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