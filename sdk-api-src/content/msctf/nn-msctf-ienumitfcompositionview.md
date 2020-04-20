---
UID: NN:msctf.IEnumITfCompositionView
title: IEnumITfCompositionView (msctf.h)
description: The IEnumITfCompositionView interface is implemented by the TSF manager to provide an enumeration of composition view objects.helpviewer_keywords: ["IEnumITfCompositionView","IEnumITfCompositionView interface [Text Services Framework]","IEnumITfCompositionView interface [Text Services Framework]","described","_tsf_ienumitfcompositionview_ref","msctf/IEnumITfCompositionView","tsf.ienumitfcompositionview"]
old-location: tsf\ienumitfcompositionview.htm
tech.root: TSF
ms.assetid: d842b367-a605-4ed0-887d-89dfcf6893a6
ms.date: 12/05/2018
ms.keywords: IEnumITfCompositionView, IEnumITfCompositionView interface [Text Services Framework], IEnumITfCompositionView interface [Text Services Framework],described, _tsf_ienumitfcompositionview_ref, msctf/IEnumITfCompositionView, tsf.ienumitfcompositionview
f1_keywords:
- msctf/IEnumITfCompositionView
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
- IEnumITfCompositionView
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# IEnumITfCompositionView interface


## -description


The <b>IEnumITfCompositionView</b> interface is implemented by the TSF manager to provide an enumeration of composition view objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumITfCompositionView</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumITfCompositionView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumITfCompositionView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumitfcompositionview-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumitfcompositionview-next">Next</a>
</td>
<td align="left" width="63%">
Obtains, from the current position, the specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumitfcompositionview-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator object by moving the current position to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumitfcompositionview-skip">Skip</a>
</td>
<td align="left" width="63%">
Moves the current position forward in the enumeration sequence by the specified number of elements.

</td>
</tr>
</table> 

