---
UID: NF:msctf.ITfCandidateListUIElement.GetSelection
title: ITfCandidateListUIElement::GetSelection
author: windows-sdk-content
description: The ITfCandidateListUIElement::GetSelection method returns the current selection of the candidate list.
old-location: tsf\itfcandidatelistuielement_getselection.htm
tech.root: TSF
ms.assetid: ac7530cd-eac8-4b2b-89e1-e05c14a81c7d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetSelection, GetSelection method [Text Services Framework], GetSelection method [Text Services Framework],ITfCandidateListUIElement interface, ITfCandidateListUIElement interface [Text Services Framework],GetSelection method, ITfCandidateListUIElement.GetSelection, ITfCandidateListUIElement::GetSelection, msctf/ITfCandidateListUIElement::GetSelection, tsf.itfcandidatelistuielement_getselection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfCandidateListUIElement.GetSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
- apiref
: 
- COM
: 
- msctf.h
: 
- ITfCandidateListUIElement.GetSelection
: 
---

# ITfCandidateListUIElement::GetSelection


## -description


The <b>ITfCandidateListUIElement::GetSelection</b> method returns the current selection of the candidate list.


## -parameters




### -param puIndex [out]

[out] A pointer to receive an index of the current selected candidate string.


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
 



