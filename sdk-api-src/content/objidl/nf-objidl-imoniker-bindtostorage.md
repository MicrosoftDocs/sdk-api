---
UID: NF:objidl.IMoniker.BindToStorage
title: IMoniker::BindToStorage (objidl.h)
description: Binds to the storage for the specified object. Unlike the IMoniker::BindToObject method, this method does not activate the object identified by the moniker.
helpviewer_keywords: ["BindToStorage","BindToStorage method [COM]","BindToStorage method [COM]","IMoniker interface","IMoniker interface [COM]","BindToStorage method","IMoniker.BindToStorage","IMoniker::BindToStorage","_com_imoniker_bindtostorage","com.imoniker_bindtostorage","objidl/IMoniker::BindToStorage"]
old-location: com\imoniker_bindtostorage.htm
tech.root: com
ms.assetid: 94c8219f-8131-45dd-b350-878ffd6161ea
ms.date: 12/05/2018
ms.keywords: BindToStorage, BindToStorage method [COM], BindToStorage method [COM],IMoniker interface, IMoniker interface [COM],BindToStorage method, IMoniker.BindToStorage, IMoniker::BindToStorage, _com_imoniker_bindtostorage, com.imoniker_bindtostorage, objidl/IMoniker::BindToStorage
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
 - IMoniker::BindToStorage
 - objidl/IMoniker::BindToStorage
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
 - IMoniker.BindToStorage
---

# IMoniker::BindToStorage


## -description

Binds to the storage for the specified object. Unlike the <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">IMoniker::BindToObject</a> method, this method does not activate the object identified by the moniker.

## -parameters

### -param pbc [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface on the bind context object, which is used in this binding operation. The bind context caches objects bound during the binding process, contains parameters that apply to all operations using the bind context, and provides the means by which the moniker implementation should retrieve information about its environment.

### -param pmkToLeft [in]

If the moniker is part of a composite moniker, pointer to the moniker to the left of this moniker. This parameter is primarily used by moniker implementers to enable cooperation between the various components of a composite moniker. Moniker clients should use <b>NULL</b>.

### -param riid [in]

A reference to the identifier of the storage interface requested, whose pointer will be returned in <i>ppvObj</i>. Storage interfaces commonly requested include <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>, <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>, and <a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a>.

### -param ppvObj [out]

The address of pointer variable that receives the interface pointer requested in <i>riid</i>. Upon successful return, *<i>ppvObj</i> contains the requested interface pointer to the storage of the object the moniker identifies. When successful, the implementation must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the storage. It is the caller's responsibility to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>. If an error occurs, *<i>ppvObj</i> should be <b>NULL</b>.

## -returns

This method can return the standard return values E_UNEXPECTED, as well as the following values.

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
The binding operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_NOSTORAGE</b></dt>
</dl>
</td>
<td width="60%">
The object identified by this moniker does not have its own storage.

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
<dt><b>MK_E_CONNECTMANUALLY</b></dt>
</dl>
</td>
<td width="60%">
The operation was unable to connect to the storage, possibly because a network device could not be connected to. For more information, see <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">IMoniker::BindToObject</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_INTERMEDIATEINTERFACENOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
An intermediate object was found but it did not support an interface required to complete the binding operation. For example, an item moniker returns this value if its container does not support the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleitemcontainer">IOleItemContainer</a> interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Unable to access the storage object.

</td>
</tr>
</table>
 

This method can also return the errors associated with the <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleitemcontainer-getobject">IOleItemContainer::GetObject</a> method.

## -remarks

There is an important difference between the <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">BindToObject</a> and <b>BindToStorage</b> methods. If, for example, you have a moniker that identifies a spreadsheet object, calling <b>BindToObject</b> provides access to the spreadsheet object itself, while calling <b>BindToStorage</b> provides access to the storage object in which the spreadsheet resides. 

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Although none of the COM moniker classes call this method in their binding operations, it might be appropriate to call it in the implementation of a new moniker class. You could call this method in an implementation of <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">BindToObject</a> that requires information from the object identified by the <i>pmkToLeft</i> parameter and can get it from the persistent storage of the object without activation. For example, if your monikers are used to identify objects that can be activated without activating their containers, you may find this method useful.

A client that can read the storage of the object its moniker identifies could also call this method.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Your implementation should locate the persistent storage for the object identified by the current moniker and return the desired interface pointer. Some types of monikers represent pseudo-objects, which are objects that do not have their own persistent storage. Such objects comprise some portion of the internal state of its container, for example, a range of cells in a spreadsheet. If your moniker class identifies this type of object, your implementation of <b>BindToStorage</b> should return the error MK_E_NOSTORAGE.

If the bind context's <a href="/windows/desktop/api/objidl/ns-objidl-bind_opts">BIND_OPTS</a> structure specifies the BINDFLAGS_JUSTTESTEXISTENCE flag, your implementation has the option of returning <b>NULL</b> in <i>ppvObj</i> (although you can also ignore the flag and perform the complete binding operation).

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
This method forwards to the class moniker's <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">BindToObject</a>.

</td>
</tr>
<tr>
<td>File moniker</td>
<td>
This method opens the file specified by the path represented by the moniker and returns an <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> pointer to that file. The method supports binding to the <b>IStorage</b> interface only; if <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> or <a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a> is requested in <i>riid</i>, the method returns E_UNSPEC, and if other interfaces are requested, this method returns E_NOINTERFACE. Unless <i>pmkToLeft</i> is a class moniker, <i>pmkToLeft</i> should be <b>NULL</b>, as in the implementation of <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">IMoniker::BindToObject</a>. 

</td>
</tr>
<tr>
<td>Generic composite moniker</td>
<td>
This method recursively calls <b>BindToStorage</b> on the rightmost component of the composite, passing the rest of the composite as the <i>pmkToLeft</i> parameter for that call. 

</td>
</tr>
<tr>
<td>Item moniker</td>
<td>
If <i>pmkToLeft</i> is <b>NULL</b>, this method returns E_INVALIDARG. Otherwise, the method calls <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">IMoniker::BindToObject</a> on the <i>pmkToLeft</i> parameter, requesting an <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleitemcontainer">IOleItemContainer</a> interface pointer. The method then calls <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleitemcontainer-getobjectstorage">IOleItemContainer::GetObjectStorage</a> for the requested interface.

</td>
</tr>
<tr>
<td>OBJREF moniker</td>
<td>
This method obtains a marshaled pointer to the requested interface on the storage that contains the running object. Because the OBJREF moniker represents a running object, no activation takes place. If the represented object is no longer running, <b>BindToStorage</b> fails with E_UNEXPECTED. 

</td>
</tr>
<tr>
<td>Pointer moniker</td>
<td>
This method queries the wrapped pointer for the requested interface.

</td>
</tr>
<tr>
<td>URL moniker</td>
<td>
The system implementation of URL monikers supports <b>BindToStorage</b> for stream objects on all URLs and for storage objects in the case where the designated resource is a compound file.

Because the URL moniker supports asynchronous binding, the actual return value of its <b>BindToStorage</b> may vary depending on the object parameters established in the bind context. However, the semantics of the bind operation are identical regardless of synchronous or asynchronous usage, as follows:

<ul>
<li>
The URL moniker pulls further information for the bind operation from the bind context. For example, the moniker can obtain pointers to the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)">IBindStatusCallback</a> and <a href="/windows/desktop/api/objidl/nn-objidl-ienumformatetc">IEnumFORMATETC</a> interfaces that are registered in the bind context. Further information can include additional bind options specified on the bind context through <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-setbindoptions">IBindCtx::SetBindOptions</a>, such as the <i>dwTickCountDeadline</i> parameter or the <i>grfFlags</i> value of BIND_MAYBOTHERUSER. The moniker then queries the client by calling <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)">IBindStatusCallback::GetBindInfo</a> and initiates the bind operation with the transport and passes the resulting IBinding to the client by calling <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85)">IBindStatusCallback::OnStartBinding</a>.

</li>
<li>
If the caller requested an asynchronous <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> or <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> by specifying the BINDF_ASYNCSTORAGE flag in the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774966(v=vs.85)">BINDINFO</a> structure retrieved from the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)">IBindStatusCallback::GetBindInfo</a>, method the URL moniker returns the object as soon as possible. Calls to these <b>IStorage</b> or <b>IStream</b> objects that reference data not yet available return E_PENDING.

</li>
<li>
If the caller does not specify asynchronous <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> or <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> as described above, the URL moniker will still return an object through the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)">IBindStatusCallback::OnDataAvailable</a> method as soon as possible. However, calls to these objects that reference data not yet available will block until the data becomes available. For some applications, this will require the least modification of their existing I/O code yet may still result in improved performance depending on their access patterns.

</li>
</ul>
</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>