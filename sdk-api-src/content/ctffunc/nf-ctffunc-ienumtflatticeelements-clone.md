---
UID: NF:ctffunc.IEnumTfLatticeElements.Clone
title: IEnumTfLatticeElements::Clone (ctffunc.h)
description: IEnumTfLatticeElements::Clone method
helpviewer_keywords: ["Clone","Clone method [Text Services Framework]","Clone method [Text Services Framework]","IEnumTfLatticeElements interface","IEnumTfLatticeElements interface [Text Services Framework]","Clone method","IEnumTfLatticeElements.Clone","IEnumTfLatticeElements::Clone","_tsf_ienumtflatticeelements_clone_ref","ctffunc/IEnumTfLatticeElements::Clone","tsf.ienumtflatticeelements_clone"]
old-location: tsf\ienumtflatticeelements_clone.htm
tech.root: TSF
ms.assetid: 867fe614-d8c0-4987-b35a-bd5b175e6850
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Text Services Framework], Clone method [Text Services Framework],IEnumTfLatticeElements interface, IEnumTfLatticeElements interface [Text Services Framework],Clone method, IEnumTfLatticeElements.Clone, IEnumTfLatticeElements::Clone, _tsf_ienumtflatticeelements_clone_ref, ctffunc/IEnumTfLatticeElements::Clone, tsf.ienumtflatticeelements_clone
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
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - IEnumTfLatticeElements::Clone
 - ctffunc/IEnumTfLatticeElements::Clone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sptip.dll
api_name:
 - IEnumTfLatticeElements.Clone
---

# IEnumTfLatticeElements::Clone


## -description

Creates a copy of the enumerator object.

## -parameters

### -param ppEnum [out]

Pointer to an <a href="/windows/desktop/api/ctffunc/nn-ctffunc-ienumtflatticeelements">IEnumTfLatticeElements</a> interface pointer that receives the new enumerator.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The method is not implemented.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-ienumtflatticeelements">IEnumTfLatticeElements
      </a>