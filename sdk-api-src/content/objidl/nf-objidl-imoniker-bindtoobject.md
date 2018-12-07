---
UID: NF:objidl.IMoniker.BindToObject
title: IMoniker::BindToObject
author: windows-sdk-content
description: Binds to the specified object. The binding process involves finding the object, putting it into the running state if necessary, and providing the caller with a pointer to a specified interface on the identified object.
old-location: com\imoniker_bindtoobject.htm
tech.root: com
ms.assetid: b5ce39ff-3387-4f72-9aea-5a26eed3810c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BindToObject, BindToObject method [COM], BindToObject method [COM],IMoniker interface, IMoniker interface [COM],BindToObject method, IMoniker.BindToObject, IMoniker::BindToObject, _com_imoniker_bindtoobject, com.imoniker_bindtoobject, objidl/IMoniker::BindToObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IMoniker.BindToObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMoniker::BindToObject


## -description


Binds to the specified object. The binding process involves finding the object, putting it into the running state if necessary, and providing the caller with a pointer to a specified interface on the identified object.


## -parameters




### -param pbc [in]

A pointer to the <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> interface on the bind context object, which is used in this binding operation. The bind context caches objects bound during the binding process, contains parameters that apply to all operations using the bind context, and provides the means by which the moniker implementation should retrieve information about its environment.


### -param pmkToLeft [in]

If the moniker is part of a composite moniker, pointer to the moniker to the left of this moniker. This parameter is primarily used by moniker implementers to enable cooperation between the various components of a composite moniker. Moniker clients should use <b>NULL</b>.


### -param riidResult [in]

The IID of the interface the client wishes to use to communicate with the object that the moniker identifies.


### -param ppvResult [out]

The address of pointer variable that receives the interface pointer requested in <i>riid</i>. Upon successful return, *<i>ppvResult</i> contains the requested interface pointer to the object the moniker identifies. When successful, the implementation must call <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on the moniker. It is the caller's responsibility to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a>. If an error occurs, *<i>ppvResult</i> should be <b>NULL</b>.


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
The binding operation could not be completed within the time limit specified by the bind context's <a href="https://msdn.microsoft.com/764f09c9-ff20-4ae2-b94f-4b0a1e117e49">BIND_OPTS</a> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_CONNECTMANUALLY</b></dt>
</dl>
</td>
<td width="60%">
The binding operation requires assistance from the end user. The most common reason for returning this value is that a password is needed or that a floppy needs to be mounted. When this value is returned, retrieve the moniker that caused the error with a call to <a href="https://msdn.microsoft.com/8f423495-7a34-4901-968e-1fe204680d8a">IBindCtx::GetObjectParam</a> with the key "ConnectManually". You can then call <a href="https://msdn.microsoft.com/424036c9-c097-4507-b562-4a01f9199b1f">IMoniker::GetDisplayName</a> to get the display name, display a dialog box that communicates the desired information, such as instructions to mount a floppy or a request for a password, and then retry the binding operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_INTERMEDIATEINTERFACENOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
An intermediate object was found but it did not support an interface required to complete the binding operation. For example, an item moniker returns this value if its container does not support the <a href="https://msdn.microsoft.com/fe306a36-da24-4b1e-ab42-359d37962d36">IOleItemContainer</a> interface.

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
 

This method can also return the errors associated with the <a href="https://msdn.microsoft.com/08569037-7ecd-4e63-9f94-c2552c327800">IOleItemContainer::GetObject</a> method.




## -remarks



<b>BindToObject</b> implements the primary function of a moniker, which is to locate the object identified by the moniker and return a pointer to one of its interfaces.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
If you are using a moniker as a persistent connection between two objects, you activate the connection by calling <b>BindToObject</b>.

You typically call <b>BindToObject</b> during the following process: 

<ol>
<li>Create a bind context object with a call to the <a href="https://msdn.microsoft.com/0f0ded09-7a7c-40bb-8198-b9f5058827d4">CreateBindCtx</a> function.</li>
<li>Call <b>BindToObject</b> using the moniker, retrieving a pointer to a desired interface on the identified object.</li>
<li>Release the bind context.</li>
<li>Through the acquired interface pointer, perform the desired operations on the object.</li>
<li>When finished with the object, release the object's interface pointer. </li>
</ol>
The following code fragment illustrates these steps.

<pre class="syntax" xml:space="preserve"><code>HRESULT hr;       // An error code
IMoniker * pMnk;  // A previously acquired interface moniker

// Obtain an IBindCtx interface.
IBindCtx * pbc; 
hr = CreateBindCtx(NULL, &amp;pbc); 
if (FAILED(hr)) exit(0);  // Handle errors here. 
   
// Obtain an implementation of pCellRange. 
ICellRange * pCellRange; 
hr = pMnk-&gt;BindToObject(pbc, NULL, IID_ICellRange, &amp;pCellRange); 
if (FAILED(hr)) exit(0);  // Handle errors here. 

// Use pCellRange here. 

// Release interfaces after use. 
pbc-&gt;Release(); 
pCellRange-&gt;Release(); 
</code></pre>
You can also use the <a href="https://msdn.microsoft.com/5a022c39-fc2c-458b-9dfe-fed1255d49a4">BindMoniker</a> function when you intend only one binding operation and don't need to retain the bind context object. This helper function encapsulates the creation of the bind context, calling <b>BindToObject</b> and releasing the bind context.

COM containers that support links to objects use monikers to locate and get access to the linked object but typically do not call <b>BindToObject</b> directly. Instead, when a user activates a link in a container, the link container usually calls <a href="https://msdn.microsoft.com/fabd6a0a-7b0c-4c99-af22-8b117addd5f7">IOleObject::DoVerb</a>, using the link handler's implementation, which calls <b>BindToObject</b> on the moniker stored in the linked object (if it cannot handle the verb).

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
What your implementation does depends on whether you expect your moniker to have a prefixâ€”that is, whether you expect the <i>pmkToLeft</i> parameter to be <b>NULL</b> or not. For example, an item moniker, which identifies an object within a container, expects that <i>pmkToLeft</i> identifies the container. An item moniker consequently uses <i>pmkToLeft</i> to request services from that container. If you expect your moniker to have a prefix, you should use the <i>pmkToLeft</i> parameter (for example, calling <b>BindToObject</b> on it) to request services from the object it identifies.

If you expect your moniker to have no prefix, your <b>BindToObject</b> implementation should first check the running object table (ROT) to see whether the object is already running. To acquire a pointer to the ROT, your implementation should call <a href="https://msdn.microsoft.com/26938d07-d772-4e72-a6aa-57dd2f2cece1">IBindCtx::GetRunningObjectTable</a> on the <i>pbc</i> parameter. You can then call the <a href="https://msdn.microsoft.com/5d74b3ee-323d-43f9-8eab-0866432659de">IRunningObjectTable::GetObject</a> method to see if the current moniker has been registered in the ROT. If so, you can immediately call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> to get a pointer to the interface requested by the caller. 



When your <b>BindToObject</b> implementation binds to some object, it should use the <i>pbc</i> parameter to call <a href="https://msdn.microsoft.com/84d49231-5fdd-4a89-8e76-1f0e56bc553f">IBindCtx::RegisterObjectBound</a> to store a reference to the bound object in the bind context. This ensures that the bound object remains running until the bind context is released, which can avoid the expense of having a subsequent binding operation load it again later.

If the bind context's <a href="https://msdn.microsoft.com/764f09c9-ff20-4ae2-b94f-4b0a1e117e49">BIND_OPTS</a> structure specifies the BINDFLAGS_JUSTTESTEXISTENCE flag, your implementation has the option of returning <b>NULL</b> in <i>ppvResult</i> (although you can also ignore the flag and perform the complete binding operation).

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
If <i>pmkLeft</i> is <b>NULL</b>, calls <a href="https://msdn.microsoft.com/65e758ce-50a4-49e8-b3b2-0cd148d2781a">CoGetClassObject</a>, using the CLSID the class moniker was initialized with (in <a href="https://msdn.microsoft.com/9361b2c1-ef26-4225-92ff-e0bef0285bc4">CreateClassMoniker</a> or through <a href="https://msdn.microsoft.com/ada46dd3-e2c5-4ff5-89bd-3805f98b247b">MkParseDisplayName</a>) and the <a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a> of the current <i>pbc</i> (<a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>).

If <i>pmkLeft</i> is non-<b>NULL</b>, calls pmkLeft-&gt;BindToObject for <a href="https://msdn.microsoft.com/4f34c5a4-46c0-4391-9c64-cbb6a366e2dc">IClassActivator</a> and calls <a href="https://msdn.microsoft.com/1bbffe63-bd3a-40c8-aece-63121a437269">IClassActivator::GetClassObject</a> with the CLSID it was initialized with and the <a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a> and locale parameters of the current <i>pbc</i> (<a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>).

</td>
</tr>
<tr>
<td>File moniker</td>
<td>
When <i>pmkToLeft</i> is <b>NULL</b>, the method looks for the moniker in the ROT and, if found, queries the retrieved object for the requested interface pointer. If the moniker is not found in the ROT, the method loads the object from the file system and retrieves the requested interface pointer.

If <i>pmkLeft</i> is not <b>NULL</b>, instead of determining the class to instantiate and initialize with the contents of the file referred to by the file moniker using <a href="https://msdn.microsoft.com/dc3cb263-7b9a-45f9-8eab-3a88aa9392db">GetClassFile</a> (or other means), call pmkLeft-&gt;BindToObject for <a href="https://msdn.microsoft.com/f624f833-2b69-43bc-92cd-c4ecbe6051c5">IClassFactory</a> and <a href="https://msdn.microsoft.com/4f34c5a4-46c0-4391-9c64-cbb6a366e2dc">IClassActivator</a>, retrieve this pointer in <i>pcf</i>. If this fails with E_NOINTERFACE, return MK_E_INTERMEDIATEINTERFACENOTSUPPORTED.

If the <a href="https://msdn.microsoft.com/f624f833-2b69-43bc-92cd-c4ecbe6051c5">IClassFactory</a> pointer is successfully retrieved, call pcf-&gt;CreateInstance(IID_IPersistFile, (void**)&amp;ppf) to get a fresh instance of the class to be initialized and initialize it by using <a href="https://msdn.microsoft.com/7d34507f-8a16-43b4-8225-010798abc546">IPersistFile</a> or other appropriate means per the existing initialization paths of file moniker.

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
If <i>pmkToLeft</i> is <b>NULL</b>, this method returns E_INVALIDARG. Otherwise, the method calls <b>BindToObject</b> on the <i>pmkToLeft</i> parameter, requesting an <a href="https://msdn.microsoft.com/fe306a36-da24-4b1e-ab42-359d37962d36">IOleItemContainer</a> interface pointer. The method then calls <a href="https://msdn.microsoft.com/08569037-7ecd-4e63-9f94-c2552c327800">IOleItemContainer::GetObject</a>, passing the string contained within the moniker, and returns the requested interface pointer.

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
<li>The URL moniker pulls further information for the bind operation from the bind context. For example, the moniker can obtain pointers to the <a href="https://msdn.microsoft.com/library/ms775060(v=VS.85).aspx">IBindStatusCallback</a> and <a href="https://msdn.microsoft.com/4d180fdd-2d58-4d26-9242-6552dda0d3e6">IEnumFORMATETC</a> interfaces that are registered in the bind context. Further information can include additional bind options specified on the bind context through <a href="https://msdn.microsoft.com/9dcce48e-567e-42b4-8df2-2bc861cb5fcb">IBindCtx::SetBindOptions</a>, such as the <i>dwTickCountDeadline</i> parameter or the <i>grfFlags</i> value of BIND_MAYBOTHERUSER.</li>
<li>
Next the moniker checks the ROT of the bind context to determine whether the referenced object is already running. The moniker can obtain this information with the following calls:

<pre class="syntax" xml:space="preserve"><code>IBindCtx::GetRunningObjectTable(&amp;prot)
prot-&gt;IsRunning(this)
</code></pre>
</li>
<li>
If the object is already running, the moniker retrieves the running object with the following call:

<pre class="syntax" xml:space="preserve"><code>prot-&gt;GetObject(this, &amp;punk)
</code></pre>
</li>
<li>
Then the moniker calls <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> for the requested interface.

</li>
<li>
Otherwise, the moniker queries the client by calling <a href="https://msdn.microsoft.com/library/ms775058(v=VS.85).aspx">IBindStatusCallback::GetBindInfo</a> to obtain additional bind information. The moniker then initiates the bind operation and passes the resulting IBinding interface back to the client by calling <a href="https://msdn.microsoft.com/library/ms775065(v=VS.85).aspx">IBindStatusCallback::OnStartBinding</a>.

</li>
<li>
If in step 1 it was determined that this was an asynchronous bind, <b>BindToObject</b> returns MK_S_ASYNCHRONOUS at this point with <b>NULL</b> in <i>ppv</i>. The caller will receive the actual object pointer during the <a href="https://msdn.microsoft.com/library/ms775063(v=VS.85).aspx">IBindStatusCallback::OnObjectAvailable</a> method at some later point. The following steps then occur asynchronously to the caller, typically on another thread of execution.

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
Having determined the class, the URL moniker creates an instance using <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> of CLSCTX_SERVER asking for the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.


</li>
<li>
The URL moniker next calls the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method of the newly created object for the <a href="https://msdn.microsoft.com/library/ms775042(v=VS.85).aspx">IPersistMoniker</a> interface. If <b>QueryInterface</b> is successful, the URL moniker calls <a href="https://msdn.microsoft.com/library/ms775044(v=VS.85).aspx">IPersistMoniker::Load</a> passing itself (this) as the moniker parameter. The object typically calls <a href="https://msdn.microsoft.com/94c8219f-8131-45dd-b350-878ffd6161ea">BindToStorage</a> asking for the storage interface that they are interested in.

</li>
<li>
Otherwise, the URL moniker calls <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> for <a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a> and, if successful, calls <a href="https://msdn.microsoft.com/351e1187-9959-4542-8778-925457c3b8e3">IPersistStream::Load</a>, passing the object an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> pointer for a stream object that is being filled asynchronously by the transport.

If the class being called is not marked with the category CATID_AsyncAware, calls to <a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">ISequentialStream::Read</a> or <a href="https://msdn.microsoft.com/f0323dda-6c31-4411-bf20-9650162109c0">ISequentialStream::Write</a> that reference data not yet available block until the data becomes available. These calls block in the traditional COM sense. A message loop is entered which allows certain messages to be processed, and the <a href="https://msdn.microsoft.com/e12d48c0-5033-47a8-bdcd-e94c49857248">IMessageFilter</a> of the thread is called appropriately.

If the class is marked with the category CATID_AsyncAware, calls to <a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">ISequentialStream::Read</a> or <a href="https://msdn.microsoft.com/f0323dda-6c31-4411-bf20-9650162109c0">ISequentialStream::Write</a> that reference data not yet available return E_PENDING.

</li>
<li>
Otherwise, the URL moniker calls <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> for <a href="https://msdn.microsoft.com/7d34507f-8a16-43b4-8225-010798abc546">IPersistFile</a> and, if successful, completes the download into a temporary file. On completion, the URL moniker calls <a href="https://msdn.microsoft.com/8391aa5c-fe6e-4b03-9eef-7958f75910a5">IPersistFile::Load</a>. The created file is cached along with other Internet downloaded data. The client must be sure not to delete this file.

</li>
<li>
When the object returns from one of the various <b>Load</b> calls described in the previous steps, the URL moniker calls the <a href="https://msdn.microsoft.com/library/ms775063(v=VS.85).aspx">IBindStatusCallback::OnObjectAvailable</a> method to return the interface pointer that the client originally requested when the client called <b>BindToObject</b>.


</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/5a022c39-fc2c-458b-9dfe-fed1255d49a4">BindMoniker</a>



<a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>
 

 

