---
UID: NF:objidl.IMoniker.GetDisplayName
title: IMoniker::GetDisplayName (objidl.h)
description: Retrieves the display name for the moniker.
helpviewer_keywords: ["GetDisplayName","GetDisplayName method [COM]","GetDisplayName method [COM]","IMoniker interface","IMoniker interface [COM]","GetDisplayName method","IMoniker.GetDisplayName","IMoniker::GetDisplayName","_com_imoniker_getdisplayname","com.imoniker_getdisplayname","objidl/IMoniker::GetDisplayName"]
old-location: com\imoniker_getdisplayname.htm
tech.root: com
ms.assetid: 424036c9-c097-4507-b562-4a01f9199b1f
ms.date: 12/05/2018
ms.keywords: GetDisplayName, GetDisplayName method [COM], GetDisplayName method [COM],IMoniker interface, IMoniker interface [COM],GetDisplayName method, IMoniker.GetDisplayName, IMoniker::GetDisplayName, _com_imoniker_getdisplayname, com.imoniker_getdisplayname, objidl/IMoniker::GetDisplayName
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
 - IMoniker::GetDisplayName
 - objidl/IMoniker::GetDisplayName
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
 - IMoniker.GetDisplayName
---

# IMoniker::GetDisplayName


## -description

Retrieves the display name for the moniker.

## -parameters

### -param pbc [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface on the bind context to be used in this operation. The bind context caches objects bound during the binding process, contains parameters that apply to all operations using the bind context, and provides the means by which the moniker implementation should retrieve information about its environment.

### -param pmkToLeft [in]

If the moniker is part of a composite moniker, pointer to the moniker to the left of this moniker. This parameter is used primarily by moniker implementers to enable cooperation between the various components of a composite moniker. Moniker clients should pass <b>NULL</b>.

### -param ppszDisplayName [out]

The address of a pointer variable that receives a pointer to the display name string for the moniker. The implementation must use <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-alloc">IMalloc::Alloc</a> to allocate the string returned in <i>ppszDisplayName</i>, and the caller is responsible for calling <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-free">IMalloc::Free</a> to free it. Both the caller and the implementation of this method use the COM task allocator returned by <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc">CoGetMalloc</a>. If an error occurs, the implementation must set *<i>ppszDisplayName</i> should be set to <b>NULL</b>.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_EXCEEDEDDEADLINE</b></dt>
</dl>
</td>
<td width="60%">
The binding operation could not be completed within the time limit specified by the bind context's <a href="/windows/desktop/api/objidl/ns-objidl-bind_opts">BIND_OPTS</a> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
There is no display name.

</td>
</tr>
</table>

## -remarks

<b>GetDisplayName</b> provides a string that is a displayable representation of the moniker. A display name is not a complete representation of a moniker's internal state; it is simply a form that can be read by users. As a result, it is possible (though rare) for two different monikers to have the same display name. While there is no guarantee that the display name of a moniker can be parsed back into that moniker when calling the <a href="/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname">MkParseDisplayName</a> function with it, failure to do so is rare.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
It is possible that retrieving a moniker's display name may be an expensive operation. For efficiency, you may want to cache the results of the first successful call to <b>GetDisplayName</b>, rather than making repeated calls.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If you are writing a moniker class in which the display name does not change, simply cache the display name and supply the cached name when requested. If the display name can change over time, getting the current display name might mean that the moniker has to access the object's storage or bind to the object, either of which can be expensive operations. If this is the case, your implementation of <b>GetDisplayName</b> should return MK_E_EXCEEDEDDEADLINE if the name cannot be retrieved by the time specified in the bind context's <a href="/windows/desktop/api/objidl/ns-objidl-bind_opts">BIND_OPTS</a> structure.

A moniker that is intended to be part of a generic composite moniker should include any preceding delimiter (such as '\') as part of its display name. For example, the display name returned by an item moniker includes the delimiter specified when it was created with the <a href="/windows/desktop/api/objbase/nf-objbase-createitemmoniker">CreateItemMoniker</a> function. The display name for a file moniker does not include a delimiter because file monikers are always expected to be the leftmost component of a composite.

<h3><a id="Implementation-specific_Notes"></a><a id="implementation-specific_notes"></a><a id="IMPLEMENTATION-SPECIFIC_NOTES"></a>Implementation-specific Notes</h3>
<table>
<tr>
<th>Implementation</th>
<th>Notes</th>
</tr>
<tr>
<td>Anti-moniker</td>
<td>For each anti-moniker contained in this moniker, this method return one instance of "\..".</td>
</tr>
<tr>
<td>Class moniker</td>
<td>The display name for class monikers is of the following form: clsid:<i>string-clsid-no-curly-braces</i> *[";" <i>clsid-param</i>=<i>value</i>]:. For example, clsid:a7b90590-36fd-11cf-857d-00aa006d2ea4:.</td>
</tr>
<tr>
<td>File moniker</td>
<td>This method returns the path that the moniker represents.</td>
</tr>
<tr>
<td>Generic composite moniker</td>
<td>This method returns the concatenation of the display names returned by each component moniker of the composite.</td>
</tr>
<tr>
<td>Item moniker</td>
<td>This method returns the concatenation of the delimiter and the item name that were specified when the item moniker was created.</td>
</tr>
<tr>
<td>OBJREF moniker</td>
<td>This method obtains the display name for the OBJREF moniker. The display name is a 64-bit encoding that encapsulates the machine location, process endpoint, and interface pointer ID (IPID) of the running object. For future compatibility, the display name is restricted to characters that can be specified as part of a URL.</td>
</tr>
<tr>
<td>Pointer moniker</td>
<td>This method returns E_NOTIMPL.</td>
</tr>
<tr>
<td>URL moniker</td>
<td>The URL moniker attempts to return its full URL string. If the moniker was created with a partial URL string (see <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775103(v=vs.85)">CreateURLMonikerEx</a>), it will first attempt to find an URL moniker in the bind context under SZ_URLCONTEXT and will next look to the moniker to its left for contextual information. If it cannot return its full URL string, it will return its partial URL string.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>



<a href="/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname">MkParseDisplayName</a>