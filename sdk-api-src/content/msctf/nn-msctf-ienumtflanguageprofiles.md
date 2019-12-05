---
UID: NN:msctf.IEnumTfLanguageProfiles
title: IEnumTfLanguageProfiles (msctf.h)
description: The IEnumTfLanguageProfiles interface is implemented by the TSF manager to provide an enumeration of language profiles.
old-location: tsf\ienumtflanguageprofiles.htm
tech.root: TSF
ms.assetid: 8ac41bff-8537-4558-a92c-6e7dae6a6bdf
ms.date: 12/05/2018
ms.keywords: IEnumTfLanguageProfiles, IEnumTfLanguageProfiles interface [Text Services Framework], IEnumTfLanguageProfiles interface [Text Services Framework],described, _tsf_ienumtflanguageprofiles_ref, msctf/IEnumTfLanguageProfiles, tsf.ienumtflanguageprofiles
ms.topic: interface
f1_keywords:
- msctf/IEnumTfLanguageProfiles
dev_langs:
- c++
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
- msctf.dll
api_name:
- IEnumTfLanguageProfiles
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# IEnumTfLanguageProfiles interface


## -description


The <b>IEnumTfLanguageProfiles</b> interface is implemented by the TSF manager to provide an enumeration of language profiles.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTfLanguageProfiles</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumTfLanguageProfiles</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTfLanguageProfiles</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtflanguageprofiles-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtflanguageprofiles-next">Next</a>
</td>
<td align="left" width="63%">
Obtains the specified number of elements in the enumeration sequence from the current position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtflanguageprofiles-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator object by moving the current position to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtflanguageprofiles-skip">Skip</a>
</td>
<td align="left" width="63%">
Moves the current position forward in the enumeration sequence by the specified number of elements.

</td>
</tr>
</table> 

