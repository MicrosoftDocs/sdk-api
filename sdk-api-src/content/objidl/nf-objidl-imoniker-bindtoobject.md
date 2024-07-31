---
UID: NF:objidl.IMoniker.BindToObject
title: IMoniker::BindToObject (objidl.h)
description: Binds to the specified object. The binding process involves finding the object, putting it into the running state if necessary, and providing the caller with a pointer to a specified interface on the identified object.
helpviewer_keywords: ["BindToObject","BindToObject method [COM]","BindToObject method [COM]","IMoniker interface","IMoniker interface [COM]","BindToObject method","IMoniker.BindToObject","IMoniker::BindToObject","_com_imoniker_bindtoobject","com.imoniker_bindtoobject","objidl/IMoniker::BindToObject"]
old-location: com\imoniker_bindtoobject.htm
tech.root: com
ms.assetid: b5ce39ff-3387-4f72-9aea-5a26eed3810c
ms.date: 12/05/2018
ms.keywords: BindToObject, BindToObject method [COM], BindToObject method [COM],IMoniker interface, IMoniker interface [COM],BindToObject method, IMoniker.BindToObject, IMoniker::BindToObject, _com_imoniker_bindtoobject, com.imoniker_bindtoobject, objidl/IMoniker::BindToObject
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
 - IMoniker::BindToObject
 - objidl/IMoniker::BindToObject
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
 - IMoniker.BindToObject
---

# IMoniker::BindToObject


## -description

Binds to the specified object. The binding process involves finding the object, putting it into the running state if necessary, and providing the caller with a pointer to a specified interface on the identified object.

## -parameters

### -param pbc [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface on the bind context object, which is used in this binding operation. The bind context caches objects bound during the binding process, contains parameters that apply to all operations using the bind context, and provides the means by which the moniker implementation should retrieve information about its environment.

### -param pmkToLeft [in]

If the moniker is part of a composite moniker, pointer to the moniker to the left of this moniker. This parameter is primarily used by moniker implementers to enable cooperation between the various components of a composite moniker. Moniker clients should use <b>NULL</b>.

### -param riidResult [in]

The IID of the interface the client wishes to use to communicate with the object that the moniker identifies.

### -param ppvResult [out]

The address of pointer variable that receives the interface pointer requested in <i>riid</i>. Upon successful return, *<i>ppvResult</i> contains the requested interface pointer to the object the moniker identifies. When successful, the implementation must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the moniker. It is the caller's responsibility to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>. If an error occurs, *<i>ppvResult</i> should be <b>NULL</b>.

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
The binding operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_NOOBJECT</b></dt>
</dl>
</td>
<td width="60%">
The object identified by this moniker, or some object identified by the composite moniker of which this moniker is a part, could not be found.

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
The binding operation requires assistance from the end user. The most common reason for returning this value is that a password is needed or that a floppy needs to be mounted. When this value is returned, retrieve the moniker that caused the error with a call to <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam">IBindCtx::GetObjectParam</a> with the key "ConnectManually". You can then call <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-getdisplayname">IMoniker::GetDisplayName</a> to get the display name, display a dialog box that communicates the desired information, such as instructions to mount a floppy or a request for a password, and then retry the binding operation.

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

<b>BindToObject</b> implements the primary function of a moniker, which is to locate the object identified by the moniker and return a pointer to one of its interfaces.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
If you are using a moniker as a persistent connection between two objects, you activate the connection by calling <b>BindToObject</b>.

You typically call <b>BindToObject</b> during the following process: 

<ol>
<li>Create a bind context object with a call to the <a href="/windows/desktop/api/objbase/nf-objbase-createbindctx">CreateBindCtx</a> function.</li>
<li>Call <b>BindToObject</b> using the moniker, retrieving a pointer to a desired interface on the identified object.</li>
<li>Release the bind context.</li>
<li>Through the acquired interface pointer, perform the desired operations on the object.</li>
<li>When finished with the object, release the object's interface pointer. </li>
</ol>
The following code fragment illustrates these steps.


``` syntax
HRESULT hr;       // An error code
IMoniker * pMnk;  // A previously acquired interface moniker

// Obtain an IBindCtx interface.
IBindCtx * pbc; 
hr = CreateBindCtx(NULL, &pbc); 
if (FAILED(hr)) exit(0);  // Handle errors here. 
   
// Obtain an implementation of pCellRange. 
ICellRange * pCellRange; 
hr = pMnk->BindToObject(pbc, NULL, IID_ICellRange, &pCellRange); 
if (FAILED(hr)) exit(0);  // Handle errors here. 

// Use pCellRange here. 

// Release interfaces after use. 
pbc->Release(); 
pCellRange->Release(); 

```

You can also use the <a href="/windows/desktop/api/objbase/nf-objbase-bindmoniker">BindMoniker</a> function when you intend only one binding operation and don't need to retain the bind context object. This helper function encapsulates the creation of the bind context, calling <b>BindToObject</b> and releasing the bind context.

COM containers that support links to objects use monikers to locate and get access to the linked object but typically do not call <b>BindToObject</b> directly. Instead, when a user activates a link in a container, the link container usually calls <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-doverb">IOleObject::DoVerb</a>, using the link handler's implementation, which calls <b>BindToObject</b> on the moniker stored in the linked object (if it cannot handle the verb).

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
What your implementation does depends on whether you expect your moniker to have a prefix; that is, whether you expect the <i>pmkToLeft</i> parameter to be <b>NULL</b> or not. For example, an item moniker, which identifies an object within a container, expects that <i>pmkToLeft</i> identifies the container. An item moniker consequently uses <i>pmkToLeft</i> to request services from that container. If you expect your moniker to have a prefix, you should use the <i>pmkToLeft</i> parameter (for example, calling <b>BindToObject</b> on it) to request services from the object it identifies.

If you expect your moniker to have no prefix, your <b>BindToObject</b> implementation should first check the running object table (ROT) to see whether the object is already running. To acquire a pointer to the ROT, your implementation should call <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getrunningobjecttable">IBindCtx::GetRunningObjectTable</a> on the <i>pbc</i> parameter. You can then call the <a href="/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-getobject">IRunningObjectTable::GetObject</a> method to see if the current moniker has been registered in the ROT. If so, you can immediately call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> to get a pointer to the interface requested by the caller. 



When your <b>BindToObject</b> implementation binds to some object, it should use the <i>pbc</i> parameter to call <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectbound">IBindCtx::RegisterObjectBound</a> to store a reference to the bound object in the bind context. This ensures that the bound object remains running until the bind context is released, which can avoid the expense of having a subsequent binding operation load it again later.

If the bind context's <a href="/windows/desktop/api/objidl/ns-objidl-bind_opts">BIND_OPTS</a> structure specifies the BINDFLAGS_JUSTTESTEXISTENCE flag, your implementation has the option of returning <b>NULL</b> in <i>ppvResult</i> (although you can also ignore the flag and perform the complete binding operation).

<h3><a id="Implementation-specific_Notes"></a><a id="implementation-specific_notes"></a><a id="IMPLEMENTATION-SPECIFIC_NOTES"></a>Implementation-specific Notes</h3>
<table>
<tr>
<th>Implementation</th>
<th>Notes</th>
</tr>
<tr>
<td>Anti-moniker</td>
<td>
This method is not implemented. It returns E_NOTIMPL.

</td>
</tr>
<tr>
<td>Class moniker</td>
<td>
If <i>pmkLeft</i> is <b>NULL</b>, calls <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject">CoGetClassObject</a>, using the CLSID the class moniker was initialized with (in <a href="/windows/desktop/api/objbase/nf-objbase-createclassmoniker">CreateClassMoniker</a> or through <a href="/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname">MkParseDisplayName</a>) and the <a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-clsctx">CLSCTX</a> of the current <i>pbc</i> (<a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>).

If <i>pmkLeft</i> is non-<b>NULL</b>, calls pmkLeft-&gt;BindToObject for <a href="/windows/desktop/api/objidl/nn-objidl-iclassactivator">IClassActivator</a> and calls <a href="/windows/desktop/api/objidl/nf-objidl-iclassactivator-getclassobject">IClassActivator::GetClassObject</a> with the CLSID it was initialized with and the <a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-clsctx">CLSCTX</a> and locale parameters of the current <i>pbc</i> (<a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>).

</td>
</tr>
<tr>
<td>File moniker</td>
<td>
When <i>pmkToLeft</i> is <b>NULL</b>, the method looks for the moniker in the ROT and, if found, queries the retrieved object for the requested interface pointer. If the moniker is not found in the ROT, the method loads the object from the file system and retrieves the requested interface pointer.

If <i>pmkLeft</i> is not <b>NULL</b>, instead of determining the class to instantiate and initialize with the contents of the file referred to by the file moniker using <a href="/windows/desktop/api/objbase/nf-objbase-getclassfile">GetClassFile</a> (or other means), call pmkLeft-&gt;BindToObject for <a href="/windows/desktop/api/unknwnbase/nn-unknwnbase-iclassfactory">IClassFactory</a> and <a href="/windows/desktop/api/objidl/nn-objidl-iclassactivator">IClassActivator</a>, retrieve this pointer in <i>pcf</i>. If this fails with E_NOINTERFACE, return MK_E_INTERMEDIATEINTERFACENOTSUPPORTED.

If the <a href="/windows/desktop/api/unknwnbase/nn-unknwnbase-iclassfactory">IClassFactory</a> pointer is successfully retrieved, call pcf-&gt;CreateInstance(IID_IPersistFile, (void**)&amp;ppf) to get a fresh instance of the class to be initialized and initialize it by using <a href="/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a> or other appropriate means per the existing initialization paths of file moniker.

</td>
</tr>
<tr>
<td>Generic composite moniker</td>
<td>
If <i>pmkToLeft</i> is <b>NULL</b>, this method looks for the moniker in the ROT and, if found, queries the retrieved object for the requested interface pointer. If <i>pmkToLeft</i> is not <b>NULL</b>, the method recursively calls <b>BindToObject</b> on the rightmost component of the composite, passing the rest of the composite as the <i>pmkToLeft</i> parameter for that call.

</td>
</tr>
<tr>
<td>Item moniker</td>
<td>
If <i>pmkToLeft</i> is <b>NULL</b>, this method returns E_INVALIDARG. Otherwise, the method calls <b>BindToObject</b> on the <i>pmkToLeft</i> parameter, requesting an <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleitemcontainer">IOleItemContainer</a> interface pointer. The method then calls <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleitemcontainer-getobject">IOleItemContainer::GetObject</a>, passing the string contained within the moniker, and returns the requested interface pointer.

</td>
</tr>
<tr>
<td>OBJREF moniker</td>
<td>
The <i>pmkToLeft</i> parameter must be <b>NULL</b>. Because the OBJREF moniker represents a running object, no activation takes place. If the represented object is no longer running, <b>BindToObject</b> fails with E_UNEXPECTED.

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
Because the URL Moniker supports asynchronous binding, the actual return value of its <b>BindToObject</b> may vary depending on the object parameters established in the bind context. For more information, see below.

</td>
</tr>
</table>
 

The semantics of the bind operation for a URL moniker are identical regardless of synchronous or asynchronous usage, and are as follows:

<ol>
<li>The URL moniker pulls further information for the bind operation from the bind context. For example, the moniker can obtain pointers to the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)">IBindStatusCallback</a> and <a href="/windows/desktop/api/objidl/nn-objidl-ienumformatetc">IEnumFORMATETC</a> interfaces that are registered in the bind context. Further information can include additional bind options specified on the bind context through <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-setbindoptions">IBindCtx::SetBindOptions</a>, such as the <i>dwTickCountDeadline</i> parameter or the <i>grfFlags</i> value of BIND_MAYBOTHERUSER.</li>
<li>
Next the moniker checks the ROT of the bind context to determine whether the referenced object is already running. The moniker can obtain this information with the following calls:


``` syntax
IBindCtx::GetRunningObjectTable(&prot)
prot->IsRunning(this)

```

</li>
<li>
If the object is already running, the moniker retrieves the running object with the following call:


``` syntax
prot->GetObject(this, &punk)

```

</li>
<li>
Then the moniker calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> for the requested interface.

</li>
<li>
Otherwise, the moniker queries the client by calling <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)">IBindStatusCallback::GetBindInfo</a> to obtain additional bind information. The moniker then initiates the bind operation and passes the resulting IBinding interface back to the client by calling <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85)">IBindStatusCallback::OnStartBinding</a>.

</li>
<li>
If in step 1 it was determined that this was an asynchronous bind, <b>BindToObject</b> returns MK_S_ASYNCHRONOUS at this point with <b>NULL</b> in <i>ppv</i>. The caller will receive the actual object pointer during the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775063(v=vs.85)">IBindStatusCallback::OnObjectAvailable</a> method at some later point. The following steps then occur asynchronously to the caller, typically on another thread of execution.

</li>
<li>
The class of the resource designated by the URL Moniker is determined in one of the following ways:


<ul>
<li>
The URL moniker examines the media type of the data. If the media type is application/x-oleobject, the first 16-bytes of the actual data (Content-Body) contain the CLSID of the resource and subsequent data is to be interpreted by the class itself. For all other media types, URL Moniker looks in the system registry for the HKEY_CLASSES_ROOT\MIME\Database\Content-Type\&lt;media-type&gt;\CLSID key. Note that application/x-oleobject will be used until application/oleobject is approved.

</li>
<li>
The URL moniker matches portions of arriving data to patterns registered in the system registry under HKEY_CLASSES_ROOT\FileTypes.

</li>
<li>
Finally, if all else fails, the URL Moniker correlates the trailing extension of the resource, if any, to a CLSID using the HKEY_CLASSES_ROOT\.??? keys in the system registry, as is done by GetClassFile and the shell.

</li>
</ul>
</li>
<li>
Having determined the class, the URL moniker creates an instance using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> of CLSCTX_SERVER asking for the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.


</li>
<li>
The URL moniker next calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of the newly created object for the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)">IPersistMoniker</a> interface. If <b>QueryInterface</b> is successful, the URL moniker calls <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85)">IPersistMoniker::Load</a> passing itself (this) as the moniker parameter. The object typically calls <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtostorage">BindToStorage</a> asking for the storage interface that they are interested in.

</li>
<li>
Otherwise, the URL moniker calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> for <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a> and, if successful, calls <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststream-load">IPersistStream::Load</a>, passing the object an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> pointer for a stream object that is being filled asynchronously by the transport.

If the class being called is not marked with the category CATID_AsyncAware, calls to <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">ISequentialStream::Read</a> or <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-write">ISequentialStream::Write</a> that reference data not yet available block until the data becomes available. These calls block in the traditional COM sense. A message loop is entered which allows certain messages to be processed, and the <a href="/windows/desktop/api/objidl/nn-objidl-imessagefilter">IMessageFilter</a> of the thread is called appropriately.

If the class is marked with the category CATID_AsyncAware, calls to <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">ISequentialStream::Read</a> or <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-write">ISequentialStream::Write</a> that reference data not yet available return E_PENDING.

</li>
<li>
Otherwise, the URL moniker calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> for <a href="/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a> and, if successful, completes the download into a temporary file. On completion, the URL moniker calls <a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-load">IPersistFile::Load</a>. The created file is cached along with other Internet downloaded data. The client must be sure not to delete this file.

</li>
<li>
When the object returns from one of the various <b>Load</b> calls described in the previous steps, the URL moniker calls the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775063(v=vs.85)">IBindStatusCallback::OnObjectAvailable</a> method to return the interface pointer that the client originally requested when the client called <b>BindToObject</b>.


</li>
</ol>

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-bindmoniker">BindMoniker</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>
