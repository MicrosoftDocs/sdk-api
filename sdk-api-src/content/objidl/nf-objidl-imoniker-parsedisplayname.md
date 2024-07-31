---
UID: NF:objidl.IMoniker.ParseDisplayName
title: IMoniker::ParseDisplayName (objidl.h)
description: Converts a display name into a moniker.
helpviewer_keywords: ["IMoniker interface [COM]","ParseDisplayName method","IMoniker.ParseDisplayName","IMoniker::ParseDisplayName","ParseDisplayName","ParseDisplayName method [COM]","ParseDisplayName method [COM]","IMoniker interface","_com_imoniker_parsedisplayname","com.imoniker_parsedisplayname","objidl/IMoniker::ParseDisplayName"]
old-location: com\imoniker_parsedisplayname.htm
tech.root: com
ms.assetid: 6a5a1f14-f14f-404b-90d8-0afceafc087c
ms.date: 12/05/2018
ms.keywords: IMoniker interface [COM],ParseDisplayName method, IMoniker.ParseDisplayName, IMoniker::ParseDisplayName, ParseDisplayName, ParseDisplayName method [COM], ParseDisplayName method [COM],IMoniker interface, _com_imoniker_parsedisplayname, com.imoniker_parsedisplayname, objidl/IMoniker::ParseDisplayName
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
 - IMoniker::ParseDisplayName
 - objidl/IMoniker::ParseDisplayName
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
 - IMoniker.ParseDisplayName
---

# IMoniker::ParseDisplayName


## -description

Converts a display name into a moniker.

## -parameters

### -param pbc [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface on the bind context to be used in this binding operation. The bind context caches objects bound during the binding process, contains parameters that apply to all operations using the bind context, and provides the means by which the moniker implementation should retrieve information about its environment.

### -param pmkToLeft [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface on the moniker that has been built out of the display name up to this point.

### -param pszDisplayName [in]

The remaining display name to be parsed.

### -param pchEaten [out]

A pointer to a variable that receives the number of characters in <i>pszDisplayName</i> that were consumed in this step.

### -param ppmkOut [out]

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> pointer variable that receives the interface pointer to the moniker that was built from <i>pszDisplayName</i>. When successful, the implementation must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the new moniker; it is the caller's responsibility to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>. If an error occurs, the implementation sets *<i>ppmkOut</i> to <b>NULL</b>.

## -returns

This method can return the standard return valuesE_OUTOFMEMORY and E_UNEXPECTED, as well as the following values.

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
The parsing operation was completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_SYNTAX</b></dt>
</dl>
</td>
<td width="60%">
An error in the syntax of the input components (<i>pmkToLeft</i>, this moniker, and <i>pszDisplayName</i>). For example, a file moniker returns this error if <i>pmkToLeft</i> is non-<b>NULL</b>, and an item moniker returns it if <i>pmkToLeft</i> is <b>NULL</b>.

</td>
</tr>
</table>
 

This method can also return the errors associated with the <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">IMoniker::BindToObject</a> method.

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Moniker clients do not typically call <b>ParseDisplayName</b> directly. Instead, they call the <a href="/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname">MkParseDisplayName</a> function when they want to convert a display name into a moniker (for example, in implementing the <b>Links</b> dialog box for a container application, or for implementing a macro language that supports references to objects outside the document). That function first parses the initial portion of the display name itself.

It then calls <b>ParseDisplayName</b> on the moniker it has just created, passing the remainder of the display name and getting a new moniker in return; this step is repeated until the entire display name has been parsed.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Your implementation may be able to perform this parsing by itself if your moniker class is designed to designate only certain kinds of objects. Otherwise, you must get an <a href="/windows/desktop/api/oleidl/nn-oleidl-iparsedisplayname">IParseDisplayName</a> interface pointer for the object identified by the moniker-so-far (that is, the composition of <i>pmkToLeft</i> and this moniker) and then return the results of calling <a href="/windows/desktop/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname">IParseDisplayName::ParseDisplayName</a>.

There are different strategies for getting an <a href="/windows/desktop/api/oleidl/nn-oleidl-iparsedisplayname">IParseDisplayName</a> pointer, as follows:

<ul>
<li>You can try to get the object's CLSID (by calling <a href="/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid">IPersist::GetClassID</a> on the object) and then call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject">CoGetClassObject</a> function, requesting the <a href="/windows/desktop/api/oleidl/nn-oleidl-iparsedisplayname">IParseDisplayName</a> interface on the class factory associated with that CLSID.</li>
<li>You can try to bind to the object itself to get an <a href="/windows/desktop/api/oleidl/nn-oleidl-iparsedisplayname">IParseDisplayName</a> pointer.</li>
<li>You can try binding to the object identified by <i>pmkToLeft</i> to get an <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleitemcontainer">IOleItemContainer</a> pointer and then call <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleitemcontainer-getobject">IOleItemContainer::GetObject</a> to get an <a href="/windows/desktop/api/oleidl/nn-oleidl-iparsedisplayname">IParseDisplayName</a> pointer for the item.</li>
</ul>
Any objects that are bound should be registered with the bind context (see <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectbound">IBindCtx::RegisterObjectBound</a>) to ensure that they remain running for the duration of the parsing operation.

<h3><a id="Implementation-specific_Notes"></a><a id="implementation-specific_notes"></a><a id="IMPLEMENTATION-SPECIFIC_NOTES"></a>Implementation-specific Notes</h3>
<table>
<tr>
<th>Implementation</th>
<th>Notes</th>
</tr>
<tr>
<td>Anti-moniker</td>
<td>
This method returns E_NOTIMPL.

</td>
</tr>
<tr>
<td>Class moniker</td>
<td>
This method parses the display name by binding to itself for <a href="/windows/desktop/api/oleidl/nn-oleidl-iparsedisplayname">IParseDisplayName</a> and asking the bound object to parse the display name into a moniker, as follows.


``` syntax
  hr = BindToObject(pbc, pmkToLeft, IID_IParseDisplayName, (void**)&ppdn);
  if (SUCCEEDED(hr)) {
    hr = ppdn->ParseDisplayName(pbc, lpszDisplayName, pchEaten, ppmkOut);
    ppdn->Release();
  }
  return hr;
```

This method tries to acquire an <a href="/windows/desktop/api/oleidl/nn-oleidl-iparsedisplayname">IParseDisplayName</a> pointer, first by binding to the class factory for the object identified by the moniker and then by binding to the object itself. If either of these binding operations is successful, the file moniker passes the unparsed portion of the display name to the <a href="/windows/desktop/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname">IParseDisplayName::ParseDisplayName</a> method.

This method returns MK_E_SYNTAX if <i>pmkToLeft</i> is non-<b>NULL</b>.

</td>
</tr>
<tr>
<td>File moniker</td>
<td>
This method tries to acquire an <a href="/windows/desktop/api/oleidl/nn-oleidl-iparsedisplayname">IParseDisplayName</a> pointer, first by binding to the class factory for the object identified by the moniker and then by binding to the object itself. If either of these binding operations is successful, the file moniker passes the unparsed portion of the display name to the <a href="/windows/desktop/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname">IParseDisplayName::ParseDisplayName</a> method. 

</td>
</tr>
<tr>
<td>Generic composite moniker</td>
<td>
This method recursively calls <b>IMoniker::ParseDisplayName</b> on the rightmost component of the composite, passing everything else as the <i>pmkToLeft</i> parameter for that call.

</td>
</tr>
<tr>
<td>Item moniker</td>
<td>
If <i>pmkToLeft</i> is <b>NULL</b>, this method returns MK_E_SYNTAX. Otherwise, the method calls <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">IMoniker::BindToObject</a> on the <i>pmkToLeft</i> parameter, requesting an <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleitemcontainer">IOleItemContainer</a> interface pointer. The method then calls <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleitemcontainer-getobject">IOleItemContainer::GetObject</a>, requesting an <a href="/windows/desktop/api/oleidl/nn-oleidl-iparsedisplayname">IParseDisplayName</a> interface pointer to the object identified by the moniker, and passes the display name to <a href="/windows/desktop/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname">IParseDisplayName::ParseDisplayName</a>.

</td>
</tr>
<tr>
<td>OBJREF moniker</td>
<td>
If <i>pmkToLeft</i> is not <b>NULL</b>, this method returns MK_E_SYNTAX.

</td>
</tr>
<tr>
<td>Pointer moniker</td>
<td>
This method queries the wrapped pointer for the <a href="/windows/desktop/api/oleidl/nn-oleidl-iparsedisplayname">IParseDisplayName</a> interface and passes the display name to <a href="/windows/desktop/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname">IParseDisplayName::ParseDisplayName</a>.

</td>
</tr>
<tr>
<td>URL moniker</td>
<td>
Parses a full or partial URL string into a result moniker (ppmkOut). If <i>szDisplayName</i> represents a full URL string (for example, "http://foo.com/default.html"), the result is a new full URL moniker. If <i>szDisplayName</i> represents a partial URL string (for example, "..\default.html"), the result is a full URL that takes its context from either the bind context's SZ_URLCONTEXT object-parameter or from this URL moniker. For example, if the context moniker was "http://foo.com/pub/list.html" and <i>szDisplayName</i> was "..\default.html", the resulting URL moniker would represent "http://foo.com/default.html".

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iparsedisplayname">IParseDisplayName</a>



<a href="/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname">MkParseDisplayName</a>
