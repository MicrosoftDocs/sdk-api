---
UID: NF:objidl.IMoniker.Inverse
title: IMoniker::Inverse (objidl.h)
description: Creates a moniker that is the inverse of this moniker. When composed to the right of this moniker or one of similar structure, the moniker will compose to nothing.
helpviewer_keywords: ["IMoniker interface [COM]","Inverse method","IMoniker.Inverse","IMoniker::Inverse","Inverse","Inverse method [COM]","Inverse method [COM]","IMoniker interface","_com_imoniker_inverse","com.imoniker_inverse","objidl/IMoniker::Inverse"]
old-location: com\imoniker_inverse.htm
tech.root: com
ms.assetid: 351d5da3-043b-426a-99e9-9f882f552239
ms.date: 12/05/2018
ms.keywords: IMoniker interface [COM],Inverse method, IMoniker.Inverse, IMoniker::Inverse, Inverse, Inverse method [COM], Inverse method [COM],IMoniker interface, _com_imoniker_inverse, com.imoniker_inverse, objidl/IMoniker::Inverse
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
 - IMoniker::Inverse
 - objidl/IMoniker::Inverse
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
 - IMoniker.Inverse
---

# IMoniker::Inverse


## -description

Creates a moniker that is the inverse of this moniker. When composed to the right of this moniker or one of similar structure, the moniker will compose to nothing.

## -parameters

### -param ppmk [out]

The address of an <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> pointer variable that receives the interface pointer to a moniker that is the inverse of this moniker. When successful, the implementation must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the new inverse moniker. It is the caller's responsibility to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>. If an error occurs, the implementation should set *<i>ppmk</i> to <b>NULL</b>.

## -returns

This method can return the standard return values E_OUTOFMEMORY, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The inverse moniker has been returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_NOINVERSE</b></dt>
</dl>
</td>
<td width="60%">
The moniker class does not have an inverse.

</td>
</tr>
</table>

## -remarks

The inverse of a moniker is analogous to the ".." directory in MS-DOS file systems; the ".." directory acts as the inverse to any other directory name, because appending ".." to a directory name results in an empty path. In the same way, the inverse of a moniker typically is also the inverse of all monikers in the same class. However, it is not necessarily the inverse of a moniker of a different class.

The inverse of a composite moniker is a composite consisting of the inverses of the components of the original moniker, arranged in reverse order. For example, if the inverse of A is Inv( A ) and the composite of A, B, and C is Comp( A, B, C ), then

Inv( Comp( A, B, C ) ) is equal to Comp( Inv( C ), Inv( B ), Inv( A ) ).

Not all monikers have inverses. Most monikers that are themselves inverses, such as anti-monikers, do not have inverses. Monikers that have no inverse cannot have relative monikers formed from inside the objects they identify to other objects outside.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
An object that is using a moniker to locate another object usually does not know the class of the moniker it is using. To get the inverse of a moniker, you should always call <b>IMoniker::Inverse</b> rather than the <a href="/windows/desktop/api/objbase/nf-objbase-createantimoniker">CreateAntiMoniker</a> function, because you cannot be certain that the moniker you're using considers an anti-moniker to be its inverse. 



The <b>Inverse</b> method is also called by the implementation of the <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-relativepathto">IMoniker::RelativePathTo</a> method, to assist in constructing a relative moniker.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If your monikers have no internal structure, you can call the <a href="/windows/desktop/api/objbase/nf-objbase-createantimoniker">CreateAntiMoniker</a> function in to get an anti-moniker in your implementation of <b>IMoniker::Inverse</b>. In your implementation of <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-composewith">IMoniker::ComposeWith</a>, you need to check for the inverse you supply in the implementation of <b>Inverse</b>.

<h3><a id="Implementation-specific_Notes"></a><a id="implementation-specific_notes"></a><a id="IMPLEMENTATION-SPECIFIC_NOTES"></a>Implementation-specific Notes</h3>
<table>
<tr>
<th>Implementation</th>
<th>Notes</th>
</tr>
<tr>
<td>Anti-moniker</td>
<td>This method returns MK_E_NOINVERSE and sets *<i>ppmk</i> to <b>NULL</b>.</td>
</tr>
<tr>
<td>Class moniker</td>
<td>This method returns an anti-moniker (that is, the results of calling <a href="/windows/desktop/api/objbase/nf-objbase-createantimoniker">CreateAntiMoniker</a>).</td>
</tr>
<tr>
<td>File moniker</td>
<td>This method returns an anti-moniker (that is, the results of calling <a href="/windows/desktop/api/objbase/nf-objbase-createantimoniker">CreateAntiMoniker</a>).</td>
</tr>
<tr>
<td>Generic composite moniker</td>
<td>This method returns a composite moniker that consists of the inverses of each of the components of the original composite, stored in reverse order. For example, if the inverse of A is Inv( A ), the inverse of the composite of A, B, and C is Comp(Inv( C ), Inv( B ), Inv( A ) ).</td>
</tr>
<tr>
<td>Item moniker</td>
<td>This method returns an anti-moniker (that is, the results of calling <a href="/windows/desktop/api/objbase/nf-objbase-createantimoniker">CreateAntiMoniker</a>).</td>
</tr>
<tr>
<td>OBJREF moniker</td>
<td>This method returns an anti-moniker (that is, the results of calling <a href="/windows/desktop/api/objbase/nf-objbase-createantimoniker">CreateAntiMoniker</a>).</td>
</tr>
<tr>
<td>Pointer moniker</td>
<td>This method returns an anti-moniker (that is, the results of calling <a href="/windows/desktop/api/objbase/nf-objbase-createantimoniker">CreateAntiMoniker</a>).</td>
</tr>
<tr>
<td>URL moniker</td>
<td>This method returns MK_E_NOINVERSE and sets *<i>ppmk</i> to <b>NULL</b>.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-createantimoniker">CreateAntiMoniker</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>