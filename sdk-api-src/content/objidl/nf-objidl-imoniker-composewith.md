---
UID: NF:objidl.IMoniker.ComposeWith
title: IMoniker::ComposeWith (objidl.h)
description: Creates a new composite moniker by combining the current moniker with the specified moniker.
helpviewer_keywords: ["ComposeWith","ComposeWith method [COM]","ComposeWith method [COM]","IMoniker interface","IMoniker interface [COM]","ComposeWith method","IMoniker.ComposeWith","IMoniker::ComposeWith","_com_imoniker_composewith","com.imoniker_composewith","objidl/IMoniker::ComposeWith"]
old-location: com\imoniker_composewith.htm
tech.root: com
ms.assetid: 6e41d79c-1a57-4270-aa84-160e0639852b
ms.date: 12/05/2018
ms.keywords: ComposeWith, ComposeWith method [COM], ComposeWith method [COM],IMoniker interface, IMoniker interface [COM],ComposeWith method, IMoniker.ComposeWith, IMoniker::ComposeWith, _com_imoniker_composewith, com.imoniker_composewith, objidl/IMoniker::ComposeWith
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
 - IMoniker::ComposeWith
 - objidl/IMoniker::ComposeWith
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
 - IMoniker.ComposeWith
---

# IMoniker::ComposeWith


## -description

Creates a new composite moniker by combining the current moniker with the specified moniker.

## -parameters

### -param pmkRight [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface on the moniker to compose onto the end of this moniker.

### -param fOnlyIfNotGeneric [in]

If <b>TRUE</b>, the caller requires a nongeneric composition, so the operation should proceed only if <i>pmkRight</i> is a moniker class that this moniker can compose with in some way other than forming a generic composite. If <b>FALSE</b>, the method can create a generic composite if necessary. Most callers should set this parameter to <b>FALSE</b>.

### -param ppmkComposite [out]

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> pointer variable that receives the composite moniker pointer. When successful, the implementation must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the resulting moniker; it is the caller's responsibility to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>. If an error occurs or if the monikers compose to nothing (for example, composing an anti-moniker with an item moniker or a file moniker), *<i>ppmkComposite</i> should be set to <b>NULL</b>.

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
The monikers were successfully combined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_NEEDGENERIC</b></dt>
</dl>
</td>
<td width="60%">
Indicates that <i>fOnlyIfNotGeneric</i> was <b>TRUE</b>, but the monikers could not be composed together without creating a generic composite moniker.

</td>
</tr>
</table>

## -remarks

Joining two monikers together is called <i>composition</i>. Sometimes two monikers of the same class can be combined in what is called nongeneric composition. For example, a file moniker representing an incomplete path and another file moniker representing a relative path can be combined to form a single file moniker representing the complete path. Nongeneric composition for a given moniker class can be handled only in the implementation of <b>ComposeWith</b> for that moniker class.

Combining two monikers of any class is called <i>generic composition</i>, which can be accomplished through a call to the <a href="/windows/desktop/api/objbase/nf-objbase-creategenericcomposite">CreateGenericComposite</a> function.

Composition of monikers is an associative operation. That is, if A, B, and C are monikers, then, where Comp() represents the composition operation, Comp( Comp( A, B ), C )

is always equal to Comp( A, Comp( B, C ) ).

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
To combine two monikers, you should call <b>ComposeWith</b> rather than calling the <a href="/windows/desktop/api/objbase/nf-objbase-creategenericcomposite">CreateGenericComposite</a> function to give the first moniker a chance to perform a nongeneric composition.

An object that provides item monikers to identify its objects would call <b>ComposeWith</b> to provide a moniker that completely identifies the location of the object. This would apply, for example, to a server that supports linking to portions of a document, or to a container that supports linking to embedded objects within its documents. In such a situation, you would do the following:

<ol>
<li>Create an item moniker that identifies the object.</li>
<li>Get a moniker that identifies the object's container.</li>
<li>Call <b>ComposeWith</b> on the moniker identifying the container, passing the item moniker as the <i>pmkRight</i> parameter.</li>
</ol>
<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
You can use either nongeneric or generic composition to compose the current moniker with the moniker that pmkRight points to. If the class of the moniker indicated by <i>pmkRight</i> is the same as that of the current moniker, it is possible to use the contents of <i>pmkRight</i> to perform a more intelligent nongeneric composition.

In writing a new moniker class, you must decide if there are any kinds of monikers, whether of your own class or another class, to which you want to give special treatment. If so, implement <b>ComposeWith</b> to check whether <i>pmkRight</i> is a moniker of the type that should have this treatment. To do this, you can call the moniker's <a href="/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid">IPersist::GetClassID</a> method, or if you have defined a moniker object that supports a custom interface, you can call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the moniker for that interface. An example of special treatment would be the nongeneric composition of an absolute file moniker with a relative file moniker. The most common case of a special moniker is the inverse for your moniker class (whatever you return from your implementation of <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-inverse">IMoniker::Inverse</a>).

If <i>pmkRight</i> completely negates the receiver so that the resulting composite is empty, you should pass back <b>NULL</b> in <i>ppmkComposite</i> and return the status code S_OK.

If the <i>pmkRight</i> parameter is not of a class to which you give special treatment, examine <i>fOnlyIfNotGeneric</i> to determine what to do next. If <i>fOnlyIfNotGeneric</i> is <b>TRUE</b>, pass back <b>NULL</b> through <i>ppmkComposite</i> and return the status code MK_E_NEEDGENERIC. If <i>fOnlyIfNotGeneric</i> is <b>FALSE</b>, call the <a href="/windows/desktop/api/objbase/nf-objbase-creategenericcomposite">CreateGenericComposite</a> function to perform the composition generically.

<h3><a id="Implementation-specific_Notes"></a><a id="implementation-specific_notes"></a><a id="IMPLEMENTATION-SPECIFIC_NOTES"></a>Implementation-specific Notes</h3>
<table>
<tr>
<th>Implementation</th>
<th>Notes</th>
</tr>
<tr>
<td>Anti-moniker</td>
<td>If <i>fOnlyIfNotGeneric</i> is <b>TRUE</b>, this method sets <i>ppmkComposite</i> to <b>NULL</b> moniker and returns MK_E_NEEDGENERIC; otherwise, the method returns the result of combining the two monikers into a generic composite. Note that composing a file, item, or pointer moniker to the right of an anti-moniker produces a generic composite rather than composing to nothing, as would be the case if the order of composition were reversed. </td>
</tr>
<tr>
<td>Class moniker</td>
<td>Follows the contract and behaves like an item moniker in that it can return E_INVALIDARG and MK_E_NEEDGENERIC, and so forth.</td>
</tr>
<tr>
<td>File moniker</td>
<td>If <i>pmkRight</i> is an anti-moniker, the returned moniker is <b>NULL</b>. If <i>pmkRight</i> is a composite whose leftmost component is an anti-moniker, the returned moniker is the composite with the leftmost anti-moniker removed. If <i>pmkRight</i> is a file moniker, this method collapses the two monikers into a single file moniker, if possible. If not possible (for example, if both file monikers represent absolute paths, as in d:\work and e:\reports), the returned moniker is <b>NULL</b> and the return value is MK_E_SYNTAX. If <i>pmkRight</i> is neither an anti-moniker nor a file moniker, the method checks the <i>fOnlyIfNotGeneric</i> parameter; if it is <b>FALSE</b>, the method combines the two monikers into a generic composite; if it is <b>TRUE</b>, the method sets *<i>ppmkComposite</i> to <b>NULL</b> and returns MK_E_NEEDGENERIC.</td>
</tr>
<tr>
<td>Generic composite moniker</td>
<td>If <i>fOnlyIfNotGeneric</i> is <b>TRUE</b>, this method sets *<i>pmkComposite</i> to <b>NULL</b> and returns MK_E_NEEDGENERIC; otherwise, the method returns the result of combining the two monikers by calling the <a href="/windows/desktop/api/objbase/nf-objbase-creategenericcomposite">CreateGenericComposite</a> function.</td>
</tr>
<tr>
<td>Item moniker</td>
<td>If <i>pmkRight</i> is an anti-moniker, the returned moniker is <b>NULL</b>. If <i>pmkRight</i> is a composite whose leftmost component is an anti-moniker, the returned moniker is the composite after the leftmost anti-moniker is removed. If <i>pmkRight</i> is not an anti-moniker, the method combines the two monikers into a generic composite if <i>fOnlyIfNotGeneric</i> is <b>FALSE</b>; if <i>fOnlyIfNotGeneric</i> is <b>TRUE</b>, the method returns a <b>NULL</b> moniker and a return value of MK_E_NEEDGENERIC.</td>
</tr>
<tr>
<td>OBJREF moniker</td>
<td>If <i>pmkRight</i> is an anti-moniker, the returned moniker is <b>NULL</b>. If <i>pmkRight</i> is a composite whose leftmost component is an anti-moniker, the returned moniker is the composite with the leftmost anti-moniker removed. If <i>pmkRight</i> is neither an anti-moniker nor a composite moniker whose leftmost component is an anti-moniker, the method checks the <i>fOnlyIfNotGeneric</i> parameter. If it is <b>FALSE</b>, the method combines the two monikers into a generic composite; if it is <b>TRUE</b>, the method sets *<i>ppmkComposite</i> to <b>NULL</b> and returns MK_E_NEEDGENERIC.</td>
</tr>
<tr>
<td>Pointer moniker</td>
<td>If <i>pmkRight</i> is an anti-moniker, the returned moniker is <b>NULL</b>. If <i>pmkRight</i> is a composite whose leftmost component is an anti-moniker, the returned moniker is the composite after the leftmost anti-moniker is removed. If <i>fOnlyIfNotGeneric</i> is <b>FALSE</b>, the returned moniker is a generic composite of the two monikers; otherwise, the method sets *<i>ppmkComposite</i> to <b>NULL</b> and returns MK_E_NEEDGENERIC.</td>
</tr>
<tr>
<td>URL moniker</td>
<td>URL monikers support composition of two URLs: a base URL composed with a relative URL. This composition is done according to the RFC on relative URLs. If <i>fOnlyIfNotGeneric</i> is <b>TRUE</b>, the method returns MK_E_NEEDGENERIC. Otherwise, this method simply returns <a href="/windows/desktop/api/objbase/nf-objbase-creategenericcomposite">CreateGenericComposite</a>(this, pmkRight, ppmkComposite). </td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-creategenericcomposite">CreateGenericComposite</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>