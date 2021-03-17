---
UID: NF:objidl.IMoniker.IsEqual
title: IMoniker::IsEqual (objidl.h)
description: Determines whether this moniker is identical to the specified moniker.
helpviewer_keywords: ["IMoniker interface [COM]","IsEqual method","IMoniker.IsEqual","IMoniker::IsEqual","IsEqual","IsEqual method [COM]","IsEqual method [COM]","IMoniker interface","_com_imoniker_isequal","com.imoniker_isequal","objidl/IMoniker::IsEqual"]
old-location: com\imoniker_isequal.htm
tech.root: com
ms.assetid: 0092e93e-d87d-4b3e-b8e1-40eeaf04c43b
ms.date: 12/05/2018
ms.keywords: IMoniker interface [COM],IsEqual method, IMoniker.IsEqual, IMoniker::IsEqual, IsEqual, IsEqual method [COM], IsEqual method [COM],IMoniker interface, _com_imoniker_isequal, com.imoniker_isequal, objidl/IMoniker::IsEqual
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMoniker::IsEqual
 - objidl/IMoniker::IsEqual
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IMoniker.IsEqual
---

# IMoniker::IsEqual


## -description

Determines whether this moniker is identical to the specified moniker.

## -parameters

### -param pmkOtherMoniker [in]

A  pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface on the moniker to be used for comparison with this one (the one from which this method is called).

## -returns

This method returns S_OK to indicate that the two monikers are identical, and S_FALSE otherwise.

## -remarks

Previous implementations of the running object table (ROT) called this method. The current implementation of the ROT uses the <a href="/windows/desktop/api/objidl/nn-objidl-irotdata">IROTData</a> interface instead.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Call this method to determine whether two monikers are identical. The reduced form of a moniker is considered different from the unreduced form. You should call the <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-reduce">IMoniker::Reduce</a> method before calling <b>IsEqual</b>, because a reduced moniker is in its most specific form. <b>IsEqual</b> may return S_FALSE on two monikers before they are reduced, and S_OK after they are reduced.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Your implementation should not reduce the current moniker before performing the comparison. It is the caller's responsibility to call <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-reduce">IMoniker::Reduce</a> to compare reduced monikers.

Two monikers that compare as equal must hash to the same value using <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-hash">IMoniker::Hash</a>.

<h3><a id="Implementation-specific_Notes"></a><a id="implementation-specific_notes"></a><a id="IMPLEMENTATION-SPECIFIC_NOTES"></a>Implementation-specific Notes</h3>
<table>
<tr>
<th>Implementation</th>
<th>Notes</th>
</tr>
<tr>
<td>Anti-moniker</td>
<td>This method returns S_OK if both are anti-monikers; otherwise, it returns S_FALSE.</td>
</tr>
<tr>
<td>Class moniker</td>
<td>This method returns S_OK if <i>pmkOther</i> is a class moniker constructed with the same CLSID information as itself. Otherwise, the method returns S_FALSE. May return E_INVALIDARG if <i>pmkOther</i> is an invalid pointer.</td>
</tr>
<tr>
<td>File moniker</td>
<td>This method returns S_OK if *<i>pmkOther</i> is a file moniker and the paths for both monikers are identical (using a case-insensitive comparison). Otherwise, the method returns S_FALSE.</td>
</tr>
<tr>
<td>Generic composite moniker</td>
<td>This method returns S_OK if the components of both monikers are equal when compared in the left-to-right order.</td>
</tr>
<tr>
<td>Item moniker</td>
<td>This method returns S_OK if both monikers are item monikers and their display names are identical (using a case-insensitive comparison); otherwise, the method returns S_FALSE.</td>
</tr>
<tr>
<td>OBJREF moniker</td>
<td>This method returns S_OK if *pmkOther is an OBJREF moniker and the paths for both monikers are identical (using a case-insensitive comparison). Otherwise, the method returns S_FALSE.</td>
</tr>
<tr>
<td>Pointer moniker</td>
<td>This method returns S_OK only if both are pointer monikers and the interface pointers that they wrap are identical.</td>
</tr>
<tr>
<td>URL moniker</td>
<td>Returns S_FALSE if the other moniker (<i>pmkOtherMoniker</i>) is not an URL moniker, which it checks using <a href="/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid">IPersist::GetClassID</a> to see whether the CLSID is CLSID_URLMoniker. If the other moniker is an URL moniker, it compares the display names of the monikers for equality, returning S_OK if they are identical or S_FALSE otherwise.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>



<a href="/windows/desktop/api/objidl/nn-objidl-irotdata">IROTData</a>