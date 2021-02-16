---
UID: NF:msctf.ITfCandidateListUIElementBehavior.SetSelection
title: ITfCandidateListUIElementBehavior::SetSelection (msctf.h)
description: The ITfCandidateListUIElementBehavior::SetSelection method set the selection of the candidate list.
helpviewer_keywords: ["ITfCandidateListUIElementBehavior interface [Text Services Framework]","SetSelection method","ITfCandidateListUIElementBehavior.SetSelection","ITfCandidateListUIElementBehavior::SetSelection","SetSelection","SetSelection method [Text Services Framework]","SetSelection method [Text Services Framework]","ITfCandidateListUIElementBehavior interface","msctf/ITfCandidateListUIElementBehavior::SetSelection","tsf.itfcandidatelistuielementbehavior_setselection"]
old-location: tsf\itfcandidatelistuielementbehavior_setselection.htm
tech.root: TSF
ms.assetid: a3afdfc9-c3e7-4735-b13f-84c45230128a
ms.date: 12/05/2018
ms.keywords: ITfCandidateListUIElementBehavior interface [Text Services Framework],SetSelection method, ITfCandidateListUIElementBehavior.SetSelection, ITfCandidateListUIElementBehavior::SetSelection, SetSelection, SetSelection method [Text Services Framework], SetSelection method [Text Services Framework],ITfCandidateListUIElementBehavior interface, msctf/ITfCandidateListUIElementBehavior::SetSelection, tsf.itfcandidatelistuielementbehavior_setselection
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
 - ITfCandidateListUIElementBehavior::SetSelection
 - msctf/ITfCandidateListUIElementBehavior::SetSelection
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
 - ITfCandidateListUIElementBehavior.SetSelection
---

# ITfCandidateListUIElementBehavior::SetSelection


## -description

The <b>ITfCandidateListUIElementBehavior::SetSelection</b> method set the selection of the candidate list.

## -parameters

### -param nIndex [in]

[in] An index for the candidate string to be selected.

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
</table>

