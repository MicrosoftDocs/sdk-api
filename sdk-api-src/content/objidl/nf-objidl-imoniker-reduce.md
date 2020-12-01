---
UID: NF:objidl.IMoniker.Reduce
title: IMoniker::Reduce (objidl.h)
description: Reduces a moniker to its simplest form.
helpviewer_keywords: ["IMoniker interface [COM]","Reduce method","IMoniker.Reduce","IMoniker::Reduce","Reduce","Reduce method [COM]","Reduce method [COM]","IMoniker interface","_com_imoniker_reduce","com.imoniker_reduce","objidl/IMoniker::Reduce"]
old-location: com\imoniker_reduce.htm
tech.root: com
ms.assetid: 1d34da7b-e6cb-4daa-a155-45beb36e035b
ms.date: 12/05/2018
ms.keywords: IMoniker interface [COM],Reduce method, IMoniker.Reduce, IMoniker::Reduce, Reduce, Reduce method [COM], Reduce method [COM],IMoniker interface, _com_imoniker_reduce, com.imoniker_reduce, objidl/IMoniker::Reduce
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
 - IMoniker::Reduce
 - objidl/IMoniker::Reduce
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
 - IMoniker.Reduce
---

# IMoniker::Reduce


## -description

Reduces a moniker to its simplest form.

## -parameters

### -param pbc [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface on the bind context to be used in this binding operation. The bind context caches objects bound during the binding process, contains parameters that apply to all operations using the bind context, and provides the means by which the moniker implementation should retrieve information about its environment.

### -param dwReduceHowFar [in]

Specifies how far this moniker should be reduced. This parameter must be one of the values from the <a href="/windows/win32/api/objidl/ne-objidl-mkrreduce">MKRREDUCE</a> enumeration.

### -param ppmkToLeft [in, out]

On entry, a pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> pointer variable that contains the interface pointer to moniker to the left of this moniker. This parameter is used primarily by moniker implementers to enable cooperation between the various components of a composite moniker; moniker clients can usually pass <b>NULL</b>.

On return, *<i>ppmkToLeft</i> is usually set to <b>NULL</b>, indicating no change in the original moniker to the left. In rare situations, *<i>ppmkToLeft</i> indicates a moniker, indicating that the previous moniker to the left should be disregarded and the moniker returned through *<i>ppmkToLeft</i> is the replacement. In such a situation, the implementation must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the old moniker to the left of this moniker and must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the new returned moniker; the caller must release it later. If an error occurs, the implementation can either leave the interface pointer unchanged or set it to <b>NULL</b>.

### -param ppmkReduced [out]

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> pointer variable that receives the interface pointer to the reduced form of this moniker, which can be <b>NULL</b> if an error occurs or if this moniker is reduced to nothing. If this moniker cannot be reduced, *<i>ppmkReduced</i> is simply set to this moniker and the return value is MK_S_REDUCED_TO_SELF. If *<i>ppmkReduced</i> is non-<b>NULL</b>, the implementation must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the new moniker; it is the caller's responsibility to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>. (This is true even if *<i>ppmkReduced</i> is set to this moniker.)

## -returns

This method can return the standard return values E_OUTOFMEMORY and E_UNEXPECTED, as well as the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_S_REDUCED_TO_SELF</b></dt>
</dl>
</td>
<td width="60%">
This moniker could not be reduced any further, so <i>ppmkReduced</i> indicates this moniker.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_EXCEEDEDDEADLINE</b></dt>
</dl>
</td>
<td width="60%">
The operation could not be completed within the time limit specified by the bind context's <a href="/windows/desktop/api/objidl/ns-objidl-bind_opts">BIND_OPTS</a> structure.

</td>
</tr>
</table>

## -remarks

This method is intended for the following uses:

<ul>
<li>
Enable the construction of user-defined macros or aliases as new kinds of moniker classes. When reduced, the moniker to which the macro evaluates is returned.

</li>
<li>
Enable the construction of a kind of moniker that tracks data as it moves about. When reduced, the moniker of the data in its current location is returned.

</li>
<li>
On file systems that support an identifier-based method of accessing files that is independent of filenames; a file moniker could be reduced to a moniker which contains one of these identifiers.

</li>
</ul>
The intent of the <a href="/windows/win32/api/objidl/ne-objidl-mkrreduce">MKRREDUCE</a> flags passed in the <i>dwReduceHowFar</i> parameter is to provide the ability to programmatically reduce a moniker to a form whose display name is recognizable to the user. For example, paths in the file system, bookmarks in word-processing documents, and range names in spreadsheets are all recognizable to users. In contrast, a macro or an alias encapsulated in a moniker are not recognizable to users.



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The scenarios described above are not currently implemented by the system-supplied moniker classes.

You should call <b>Reduce</b> before comparing two monikers using the <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-isequal">IMoniker::IsEqual</a> method because a reduced moniker is in its most specific form. <b>IsEqual</b> may return S_FALSE on two monikers before they are reduced and return S_OK after they are reduced.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If the current moniker can be reduced, your implementation must not reduce the moniker in-place. Instead, it must return a new moniker that represents the reduced state of the current one. This way, the caller still has the option of using the nonreduced moniker (for example, enumerating its components). Your implementation should reduce the moniker at least as far as is requested.

<h3><a id="Implementation-specific_Notes"></a><a id="implementation-specific_notes"></a><a id="IMPLEMENTATION-SPECIFIC_NOTES"></a>Implementation-specific Notes</h3>
<table>
<tr>
<th>Implementation</th>
<th>Notes</th>
</tr>
<tr>
<td>Anti-moniker</td>
<td>This method returns MK_S_REDUCED_TO_SELF and passes back the same moniker.</td>
</tr>
<tr>
<td>Class moniker</td>
<td>This method returns MK_S_REDUCED_TO_SELF and passes back the same moniker.</td>
</tr>
<tr>
<td>File moniker</td>
<td>This method returns MK_S_REDUCED_TO_SELF and passes back the same moniker.</td>
</tr>
<tr>
<td>Generic composite moniker</td>
<td>This method recursively calls <b>Reduce</b> for each of its component monikers. If any of the components reduces itself, the method returns S_OK and passes back a composite of the reduced components. If no reduction occurred, the method passes back the same moniker and returns MK_S_REDUCED_TO_SELF.</td>
</tr>
<tr>
<td>Item moniker</td>
<td>This method returns MK_S_REDUCED_TO_SELF and passes back the same moniker.</td>
</tr>
<tr>
<td>OBJREF moniker</td>
<td>This method returns MK_S_REDUCED_TO_SELF and passes back the same moniker.</td>
</tr>
<tr>
<td>Pointer moniker</td>
<td>This method returns MK_S_REDUCED_TO_SELF and passes back the same moniker.</td>
</tr>
<tr>
<td>URL moniker</td>
<td>This method returns MK_S_REDUCED_TO_SELF and passes back the same moniker.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>