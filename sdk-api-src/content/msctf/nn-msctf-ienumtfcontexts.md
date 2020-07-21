---
UID: NN:msctf.IEnumTfContexts
title: IEnumTfContexts (msctf.h)
description: The IEnumTfContexts interface is implemented by the TSF manager to provide an enumeration of context objects.
helpviewer_keywords: ["IEnumTfContexts","IEnumTfContexts interface [Text Services Framework]","IEnumTfContexts interface [Text Services Framework]","described","_tsf_ienumtfcontexts_ref","msctf/IEnumTfContexts","tsf.ienumtfcontexts"]
old-location: tsf\ienumtfcontexts.htm
tech.root: TSF
ms.assetid: 20b342e6-cac4-4bc5-820b-e397e0ce4648
ms.date: 12/05/2018
ms.keywords: IEnumTfContexts, IEnumTfContexts interface [Text Services Framework], IEnumTfContexts interface [Text Services Framework],described, _tsf_ienumtfcontexts_ref, msctf/IEnumTfContexts, tsf.ienumtfcontexts
f1_keywords:
- msctf/IEnumTfContexts
dev_langs:
- c++
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
- msctf.dll
api_name:
- IEnumTfContexts
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# IEnumTfContexts interface


## -description


The <b>IEnumTfContexts</b> interface is implemented by the TSF manager to provide an enumeration of context objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTfContexts</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumTfContexts</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTfContexts</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfcontexts-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfcontexts-next">Next</a>
</td>
<td align="left" width="63%">
Obtains, from the current position, the specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfcontexts-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator object by moving the current position to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfcontexts-skip">Skip</a>
</td>
<td align="left" width="63%">
Moves the current position forward in the enumeration sequence by the specified number of elements.

</td>
</tr>
</table> 

