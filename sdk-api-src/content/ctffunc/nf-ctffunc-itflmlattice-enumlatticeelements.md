---
UID: NF:ctffunc.ITfLMLattice.EnumLatticeElements
title: ITfLMLattice::EnumLatticeElements (ctffunc.h)
description: ITfLMLattice::EnumLatticeElements method
helpviewer_keywords: ["EnumLatticeElements","EnumLatticeElements method [Text Services Framework]","EnumLatticeElements method [Text Services Framework]","ITfLMLattice interface","ITfLMLattice interface [Text Services Framework]","EnumLatticeElements method","ITfLMLattice.EnumLatticeElements","ITfLMLattice::EnumLatticeElements","_tsf_itflmlattice_enumlatticeelements_ref","ctffunc/ITfLMLattice::EnumLatticeElements","tsf.itflmlattice_enumlatticeelements"]
old-location: tsf\itflmlattice_enumlatticeelements.htm
tech.root: TSF
ms.assetid: c42ad69f-d27a-40b7-8d63-3b422cb69db5
ms.date: 12/05/2018
ms.keywords: EnumLatticeElements, EnumLatticeElements method [Text Services Framework], EnumLatticeElements method [Text Services Framework],ITfLMLattice interface, ITfLMLattice interface [Text Services Framework],EnumLatticeElements method, ITfLMLattice.EnumLatticeElements, ITfLMLattice::EnumLatticeElements, _tsf_itflmlattice_enumlatticeelements_ref, ctffunc/ITfLMLattice::EnumLatticeElements, tsf.itflmlattice_enumlatticeelements
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
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfLMLattice::EnumLatticeElements
 - ctffunc/ITfLMLattice::EnumLatticeElements
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
 - ITfLMLattice.EnumLatticeElements
---

# ITfLMLattice::EnumLatticeElements


## -description

Obtains an enumerator that contains all lattice elements contained in the lattice property that start at or after a specific offset from the start of the frame.

## -parameters

### -param dwFrameStart [in]

Specifies the offset, in 100-nanosecond units, relative to the start of the phrase, of the first element to obtain.

### -param rguidType [in]

Specifies the lattice type identifier. This can be one of the <a href="/windows/desktop/TSF/lattice-types">Lattice Type</a> values.

### -param ppEnum [out]

Pointer to an <a href="/windows/desktop/api/ctffunc/nn-ctffunc-ienumtflatticeelements">IEnumTfLatticeElements</a> interface pointer that receives the enumerator object.

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
<i>rguidType</i> is unsupported by the lattice property.

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
</table>

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-ienumtflatticeelements">IEnumTfLatticeElements
      </a>



<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itflmlattice">ITfLMLattice</a>



<a href="/windows/desktop/TSF/lattice-types">Lattice Types
      </a>