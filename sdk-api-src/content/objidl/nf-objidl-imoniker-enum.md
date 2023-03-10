---
UID: NF:objidl.IMoniker.Enum
title: IMoniker::Enum (objidl.h)
description: Retrieves a pointer to an enumerator for the components of a composite moniker.
helpviewer_keywords: ["Enum","Enum method [COM]","Enum method [COM]","IMoniker interface","IMoniker interface [COM]","Enum method","IMoniker.Enum","IMoniker::Enum","_com_imoniker_enum","com.imoniker_enum","objidl/IMoniker::Enum"]
old-location: com\imoniker_enum.htm
tech.root: com
ms.assetid: 7e2e4d92-d5dd-4294-944e-8b1e88901ee1
ms.date: 12/05/2018
ms.keywords: Enum, Enum method [COM], Enum method [COM],IMoniker interface, IMoniker interface [COM],Enum method, IMoniker.Enum, IMoniker::Enum, _com_imoniker_enum, com.imoniker_enum, objidl/IMoniker::Enum
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
 - IMoniker::Enum
 - objidl/IMoniker::Enum
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
 - IMoniker.Enum
---

# IMoniker::Enum


## -description

Retrieves a pointer to an enumerator for the components of a composite moniker.

## -parameters

### -param fForward [in]

If <b>TRUE</b>, enumerates the monikers from left to right. If <b>FALSE</b>, enumerates from right to left.

### -param ppenumMoniker [out]

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-ienummoniker">IEnumMoniker</a> pointer variable that receives the interface pointer to the enumerator object for the moniker. When successful, the implementation must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the enumerator object. It is the caller's responsibility to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>. If an error occurs or if the moniker has no enumerable components, the implementation sets *<i>ppenumMoniker</i> to <b>NULL</b>.

## -returns

This method can return the standard return values E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.

## -remarks

This method must supply an <a href="/windows/desktop/api/objidl/nn-objidl-ienummoniker">IEnumMoniker</a> pointer to an enumerator that can enumerate the components of a moniker. For example, the implementation of the <b>IMoniker::Enum</b> method for a generic composite moniker creates an enumerator that can determine the individual monikers that make up the composite, while the <b>IMoniker::Enum</b> method for a file moniker creates an enumerator that returns monikers representing each of the components in the path.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Call this method to examine the components that make up a composite moniker.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If the new moniker class has no discernible internal structure, your implementation of this method can simply return S_OK and set <i>ppenumMoniker</i> to <b>NULL</b>.

<h3><a id="Implementation-specific_Notes"></a><a id="implementation-specific_notes"></a><a id="IMPLEMENTATION-SPECIFIC_NOTES"></a>Implementation-specific Notes</h3>
<table>
<tr>
<th>Implementation</th>
<th>Notes</th>
</tr>
<tr>
<td>Anti-moniker</td>
<td>This method returns S_OK and sets <i>ppenumMoniker</i> to <b>NULL</b>.</td>
</tr>
<tr>
<td>Class moniker</td>
<td>This method returns S_OK and sets <i>ppenumMoniker</i> to <b>NULL</b>.</td>
</tr>
<tr>
<td>File moniker</td>
<td>This method returns S_OK and sets <i>ppenumMoniker</i> to <b>NULL</b>.</td>
</tr>
<tr>
<td>Generic composite moniker</td>
<td>If successful, this method returns S_OK and passes back an enumerator that enumerates the component monikers that make up the composite; otherwise, the method returns E_OUTOFMEMORY. </td>
</tr>
<tr>
<td>Item moniker</td>
<td>This method returns S_OK and sets <i>ppenumMoniker</i> to <b>NULL</b>.</td>
</tr>
<tr>
<td>OBJREF moniker</td>
<td>This method returns S_OK and sets <i>ppenumMoniker</i> to <b>NULL</b>.</td>
</tr>
<tr>
<td>Pointer moniker</td>
<td>This method returns E_NOTIMPL.</td>
</tr>
<tr>
<td>URL moniker</td>
<td>This method returns S_OK and sets <i>ppenumMoniker</i> to <b>NULL</b>.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ienummoniker">IEnumMoniker</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>