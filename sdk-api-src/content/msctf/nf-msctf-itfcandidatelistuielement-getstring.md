---
UID: NF:msctf.ITfCandidateListUIElement.GetString
title: ITfCandidateListUIElement::GetString (msctf.h)
description: The ITfCandidateListUIElement::GetString method returns the string of the index.
helpviewer_keywords: ["GetString","GetString method [Text Services Framework]","GetString method [Text Services Framework]","ITfCandidateListUIElement interface","ITfCandidateListUIElement interface [Text Services Framework]","GetString method","ITfCandidateListUIElement.GetString","ITfCandidateListUIElement::GetString","msctf/ITfCandidateListUIElement::GetString","tsf.itfcandidatelistuielement_getstring"]
old-location: tsf\itfcandidatelistuielement_getstring.htm
tech.root: TSF
ms.assetid: 85cf60e3-f068-499f-b726-9ccea3cd8503
ms.date: 12/05/2018
ms.keywords: GetString, GetString method [Text Services Framework], GetString method [Text Services Framework],ITfCandidateListUIElement interface, ITfCandidateListUIElement interface [Text Services Framework],GetString method, ITfCandidateListUIElement.GetString, ITfCandidateListUIElement::GetString, msctf/ITfCandidateListUIElement::GetString, tsf.itfcandidatelistuielement_getstring
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
 - ITfCandidateListUIElement::GetString
 - msctf/ITfCandidateListUIElement::GetString
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
 - ITfCandidateListUIElement.GetString
---

# ITfCandidateListUIElement::GetString


## -description

The <b>ITfCandidateListUIElement::GetString</b> method returns the string of the index.

## -parameters

### -param uIndex [in]

[in] An index of the string to obtain.

### -param pstr [out]

[out] A pointer to BSTR for the candidate string of the index.

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

