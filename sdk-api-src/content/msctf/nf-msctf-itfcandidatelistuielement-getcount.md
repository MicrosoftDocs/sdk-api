---
UID: NF:msctf.ITfCandidateListUIElement.GetCount
title: ITfCandidateListUIElement::GetCount
author: windows-sdk-content
description: The ITfCandidateListUIElement::GetCount method returns the count of the candidate strings.
old-location: tsf\itfcandidatelistuielement_getcount.htm
tech.root: TSF
ms.assetid: 9009203a-71d1-49b2-823d-d6f04bf3743b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCount, GetCount method [Text Services Framework], GetCount method [Text Services Framework],ITfCandidateListUIElement interface, ITfCandidateListUIElement interface [Text Services Framework],GetCount method, ITfCandidateListUIElement.GetCount, ITfCandidateListUIElement::GetCount, msctf/ITfCandidateListUIElement::GetCount, tsf.itfcandidatelistuielement_getcount
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
 - ITfCandidateListUIElement.GetCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfCandidateListUIElement::GetCount


## -description


The <b>ITfCandidateListUIElement::GetCount</b> method returns the count of the candidate strings.


## -parameters




### -param puCount [out]

[out] A pointer to receive a count of the candidate strings.


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
 



