---
UID: NF:objidl.IMoniker.GetTimeOfLastChange
title: IMoniker::GetTimeOfLastChange (objidl.h)
description: Retrieves the time at which the object identified by this moniker was last changed.
helpviewer_keywords: ["GetTimeOfLastChange","GetTimeOfLastChange method [COM]","GetTimeOfLastChange method [COM]","IMoniker interface","IMoniker interface [COM]","GetTimeOfLastChange method","IMoniker.GetTimeOfLastChange","IMoniker::GetTimeOfLastChange","_com_imoniker_gettimeoflastchange","com.imoniker_gettimeoflastchange","objidl/IMoniker::GetTimeOfLastChange"]
old-location: com\imoniker_gettimeoflastchange.htm
tech.root: com
ms.assetid: 120cc951-6797-4ef6-890b-57ff8d3d23ba
ms.date: 12/05/2018
ms.keywords: GetTimeOfLastChange, GetTimeOfLastChange method [COM], GetTimeOfLastChange method [COM],IMoniker interface, IMoniker interface [COM],GetTimeOfLastChange method, IMoniker.GetTimeOfLastChange, IMoniker::GetTimeOfLastChange, _com_imoniker_gettimeoflastchange, com.imoniker_gettimeoflastchange, objidl/IMoniker::GetTimeOfLastChange
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
 - IMoniker::GetTimeOfLastChange
 - objidl/IMoniker::GetTimeOfLastChange
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
 - IMoniker.GetTimeOfLastChange
---

# IMoniker::GetTimeOfLastChange


## -description

Retrieves the time at which the object identified by this moniker was last changed.

## -parameters

### -param pbc [in]

A pointer to the bind context to be used in this binding operation. The bind context caches objects bound during the binding process, contains parameters that apply to all operations using the bind context, and provides the means by which the moniker implementation should retrieve information about its environment. For more information, see <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>.

### -param pmkToLeft [in]

If the moniker is part of a composite moniker, pointer to the moniker to the left of this moniker. This parameter is primarily used by moniker implementers to enable cooperation between the various components of a composite moniker. Moniker clients should pass <b>NULL</b>.

### -param pFileTime [out]

A pointer to the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that receives the time of last change. A value of {0xFFFFFFFF,0x7FFFFFFF} indicates an error (for example, exceeded time limit, information not available).

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
<dt><b>MK_E_CONNECTMANUALLY</b></dt>
</dl>
</td>
<td width="60%">
The operation was unable to connect to the storage for this object, possibly because a network device could not be connected to. For more information, see <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">IMoniker::BindToObject</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The time of the change is unavailable and will not be available regardless of the deadline that is used.

</td>
</tr>
</table>

## -remarks

To be precise, the time returned is the earliest time COM can identify after which no change has occurred, so this time may be later than the time of the last change to the object.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
If you're caching information returned by the object identified by the moniker, you may want to ensure that your information is up-to-date. To do so, you would call <b>GetTimeOfLastChange</b> and compare the time returned with the time you last retrieved information from the object. 



For the monikers stored within linked objects, <b>GetTimeOfLastChange</b> is primarily called by the default handler's implementation of <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-isuptodate">IOleObject::IsUpToDate</a>. Container applications call <b>IOleObject::IsUpToDate</b> to determine if a linked object (or an embedded object containing linked objects) is up-to-date without actually binding to the object. This enables an application to determine quickly which linked objects require updating when the end user opens a document. The application can then bind only those linked objects that need updating (after prompting the end user to determine whether they should be updated) instead of binding every linked object in the document.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
It is important to perform this operation quickly because, for linked objects, this method is called when a user first opens a compound document. Consequently, your <b>GetTimeOfLastChange</b> implementation should not bind to any objects. In addition, your implementation should check the deadline parameter in the bind context and return MK_E_EXCEEDEDDEADLINE if the operation cannot be completed by the specified time.

Following are some strategies you can use in your implementations: 



<ul>
<li>
For many types of monikers, the pmkToLeft parameter identifies the container of the object identified by this moniker. If this is true of your moniker class, you can simply call <b>GetTimeOfLastChange</b> on the <i>pmkToLeft</i> parameter, because an object cannot have changed at a date later than its container.

</li>
<li>
You can get a pointer to the running object table (ROT) by calling <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getrunningobjecttable">IBindCtx::GetRunningObjectTable</a> on the <i>pbc</i> parameter and then calling <a href="/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-gettimeoflastchange">IRunningObjectTable::GetTimeOfLastChange</a>, because the ROT generally records the time of last change.

</li>
<li>
You can get the storage associated with this moniker (or the <i>pmkToLeft</i> moniker) and return the storage's last modification time with a call to <a href="/windows/desktop/api/objidl/nf-objidl-istorage-stat">IStorage::Stat</a>.

</li>
</ul>
<h3><a id="Implementation-specific_Notes"></a><a id="implementation-specific_notes"></a><a id="IMPLEMENTATION-SPECIFIC_NOTES"></a>Implementation-specific Notes</h3>
<table>
<tr>
<th>Implementation</th>
<th>Notes</th>
</tr>
<tr>
<td>Anti-moniker</td>
<td>This method returns E_NOTIMPL.</td>
</tr>
<tr>
<td>Class moniker</td>
<td>This method returns MK_E_UNAVAILABLE.</td>
</tr>
<tr>
<td>File moniker</td>
<td>If this moniker is in the ROT, this method returns the last change time registered there; otherwise, it returns the last write time for the file. If the file cannot be found, this method returns MK_E_NOOBJECT.</td>
</tr>
<tr>
<td>Generic composite moniker</td>
<td>This method creates a composite of <i>pmkToLeft</i> (if non-<b>NULL</b>) and this moniker and uses the ROT to retrieve the time of last change. If the object is not in the ROT, the method recursively calls <b>GetTimeOfLastChange</b> on the rightmost component of the composite, passing the remainder of the composite as the <i>pmkToLeft</i> parameter for that call.</td>
</tr>
<tr>
<td>Item moniker</td>
<td>If <i>pmkToLeft</i> is <b>NULL</b>, this method returns MK_E_NOTBINDABLE. Otherwise, the method creates a composite of <i>pmkToLeft</i> and this moniker and uses the ROT to access the time of last change. If the object is not in the ROT, the method calls <b>GetTimeOfLastChange</b> on the <i>pmkToLeft</i> parameter.</td>
</tr>
<tr>
<td>OBJREF moniker</td>
<td>This method returns E_NOTIMPL.</td>
</tr>
<tr>
<td>Pointer moniker</td>
<td>This method returns E_NOTIMPL.</td>
</tr>
<tr>
<td>URL moniker</td>
<td>This method returns the time of last change of an object that is registered in the ROT.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>



<a href="/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-gettimeoflastchange">IRunningObjectTable::GetTimeOfLastChange</a>