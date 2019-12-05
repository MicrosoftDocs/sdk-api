---
UID: NN:ctffunc.IEnumTfLatticeElements
title: IEnumTfLatticeElements (ctffunc.h)
description: The IEnumTfLatticeElements interface is implemented by the TSF manager to provide an enumeration of lattice elements.
old-location: tsf\ienumtflatticeelements.htm
tech.root: TSF
ms.assetid: 5e36f052-a539-4020-8899-fb14c792c666
ms.date: 12/05/2018
ms.keywords: IEnumTfLatticeElements, IEnumTfLatticeElements interface [Text Services Framework], IEnumTfLatticeElements interface [Text Services Framework],described, _tsf_ienumtflatticeelements_ref, ctffunc/IEnumTfLatticeElements, tsf.ienumtflatticeelements
ms.topic: interface
f1_keywords:
- ctffunc/IEnumTfLatticeElements
dev_langs:
- c++
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Sptip.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Sptip.dll
api_name:
- IEnumTfLatticeElements
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# IEnumTfLatticeElements interface


## -description


The <b>IEnumTfLatticeElements</b> interface is implemented by the TSF manager to provide an enumeration of lattice elements.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTfLatticeElements</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumTfLatticeElements</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTfLatticeElements</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-ienumtflatticeelements-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-ienumtflatticeelements-next">Next</a>
</td>
<td align="left" width="63%">
Obtains the specified number of elements in the enumeration sequence from the current position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-ienumtflatticeelements-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator object by moving the current position to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-ienumtflatticeelements-skip">Skip</a>
</td>
<td align="left" width="63%">
Moves the current position forward in the enumeration sequence by the specified number of elements.

</td>
</tr>
</table> 

