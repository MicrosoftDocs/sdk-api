---
UID: NF:msctf.ITfCandidateListUIElement.GetUpdatedFlags
title: ITfCandidateListUIElement::GetUpdatedFlags (msctf.h)
description: The ITfCandidateListUIElement::GetUpdatedFlags method returns the flag that tells which part of this element was updated.
helpviewer_keywords: ["GetUpdatedFlags","GetUpdatedFlags method [Text Services Framework]","GetUpdatedFlags method [Text Services Framework]","ITfCandidateListUIElement interface","ITfCandidateListUIElement interface [Text Services Framework]","GetUpdatedFlags method","ITfCandidateListUIElement.GetUpdatedFlags","ITfCandidateListUIElement::GetUpdatedFlags","TF_CLUIE_COUNT","TF_CLUIE_CURRENTPAGE","TF_CLUIE_DOCUMENTMGR","TF_CLUIE_PAGEINDEX","TF_CLUIE_SELECTION","TF_CLUIE_STRING","msctf/ITfCandidateListUIElement::GetUpdatedFlags","tsf.itfcandidatelistuielement_getupdatedflags"]
old-location: tsf\itfcandidatelistuielement_getupdatedflags.htm
tech.root: TSF
ms.assetid: 618bf940-3145-4da5-a253-620b17b045c8
ms.date: 12/05/2018
ms.keywords: GetUpdatedFlags, GetUpdatedFlags method [Text Services Framework], GetUpdatedFlags method [Text Services Framework],ITfCandidateListUIElement interface, ITfCandidateListUIElement interface [Text Services Framework],GetUpdatedFlags method, ITfCandidateListUIElement.GetUpdatedFlags, ITfCandidateListUIElement::GetUpdatedFlags, TF_CLUIE_COUNT, TF_CLUIE_CURRENTPAGE, TF_CLUIE_DOCUMENTMGR, TF_CLUIE_PAGEINDEX, TF_CLUIE_SELECTION, TF_CLUIE_STRING, msctf/ITfCandidateListUIElement::GetUpdatedFlags, tsf.itfcandidatelistuielement_getupdatedflags
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
 - ITfCandidateListUIElement::GetUpdatedFlags
 - msctf/ITfCandidateListUIElement::GetUpdatedFlags
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
 - ITfCandidateListUIElement.GetUpdatedFlags
---

# ITfCandidateListUIElement::GetUpdatedFlags


## -description

The <b>ITfCandidateListUIElement::GetUpdatedFlags</b> method returns the flag that tells which part of this element was updated.

## -parameters

### -param pdwFlags [out]

[out] a pointer to receive the flags that is a combination of the following bits:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_CLUIE_DOCUMENTMGR"></a><a id="tf_cluie_documentmgr"></a><dl>
<dt><b>TF_CLUIE_DOCUMENTMGR</b></dt>
</dl>
</td>
<td width="60%">
The target document manager was changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_CLUIE_COUNT"></a><a id="tf_cluie_count"></a><dl>
<dt><b>TF_CLUIE_COUNT</b></dt>
</dl>
</td>
<td width="60%">
The count of the candidate string was changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_CLUIE_SELECTION"></a><a id="tf_cluie_selection"></a><dl>
<dt><b>TF_CLUIE_SELECTION</b></dt>
</dl>
</td>
<td width="60%">
The selection of the candidate was changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_CLUIE_STRING"></a><a id="tf_cluie_string"></a><dl>
<dt><b>TF_CLUIE_STRING</b></dt>
</dl>
</td>
<td width="60%">
Some strings in the list were changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_CLUIE_PAGEINDEX"></a><a id="tf_cluie_pageindex"></a><dl>
<dt><b>TF_CLUIE_PAGEINDEX</b></dt>
</dl>
</td>
<td width="60%">
The current page index or some page index was changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_CLUIE_CURRENTPAGE"></a><a id="tf_cluie_currentpage"></a><dl>
<dt><b>TF_CLUIE_CURRENTPAGE</b></dt>
</dl>
</td>
<td width="60%">
The page was changed.

</td>
</tr>
</table>

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

