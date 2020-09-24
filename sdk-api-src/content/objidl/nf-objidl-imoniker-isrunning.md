---
UID: NF:objidl.IMoniker.IsRunning
title: IMoniker::IsRunning (objidl.h)
description: Determines whether the object identified by this moniker is currently loaded and running.
helpviewer_keywords: ["IMoniker interface [COM]","IsRunning method","IMoniker.IsRunning","IMoniker::IsRunning","IsRunning","IsRunning method [COM]","IsRunning method [COM]","IMoniker interface","_com_imoniker_isrunning","com.imoniker_isrunning","objidl/IMoniker::IsRunning"]
old-location: com\imoniker_isrunning.htm
tech.root: com
ms.assetid: 081b394c-1fe8-4519-999e-b3985a77bd9c
ms.date: 12/05/2018
ms.keywords: IMoniker interface [COM],IsRunning method, IMoniker.IsRunning, IMoniker::IsRunning, IsRunning, IsRunning method [COM], IsRunning method [COM],IMoniker interface, _com_imoniker_isrunning, com.imoniker_isrunning, objidl/IMoniker::IsRunning
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
 - IMoniker::IsRunning
 - objidl/IMoniker::IsRunning
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
 - IMoniker.IsRunning
---

# IMoniker::IsRunning


## -description

Determines whether the object identified by this moniker is currently loaded and running.

## -parameters

### -param pbc [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface on the bind context to be used in this binding operation. The bind context caches objects bound during the binding process, contains parameters that apply to all operations using the bind context, and provides the means by which the moniker implementation should retrieve information about its environment.

### -param pmkToLeft [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface on the moniker to the left of this moniker if this moniker is part of a composite. This parameter is used primarily by moniker implementers to enable cooperation between the various components of a composite moniker; moniker clients can usually pass <b>NULL</b>.

### -param pmkNewlyRunning [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface on the moniker most recently added to the running object table (ROT). This can be <b>NULL</b>. If non-<b>NULL</b>, the implementation can return the results of calling <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-isequal">IMoniker::IsEqual</a> on the <i>pmkNewlyRunning</i> parameter, passing the current moniker. This parameter is intended to enable <b>IsRunning</b> implementations that are more efficient than just searching the ROT, but the implementation can choose to ignore <i>pmkNewlyRunning</i> without causing any harm.

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
The moniker is running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The moniker is not running.

</td>
</tr>
</table>

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
If speed is important when you're requesting services from the object identified by the moniker, you may want those services only if the object is already running (because loading an object into the running state may be time-consuming). In such a situation, you should call <b>IsRunning</b> to determine whether the object is running.

For the monikers stored within linked objects, <b>IsRunning</b> is primarily called by the default handler's implementation of <a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-bindifrunning">IOleLink::BindIfRunning</a>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
To get a pointer to the ROT, your implementation should call <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getrunningobjecttable">IBindCtx::GetRunningObjectTable</a> on the <i>pbc</i> parameter. Your implementation can then call <a href="/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-isrunning">IRunningObjectTable::IsRunning</a> to determine whether the object identified by the moniker is running. The object identified by the moniker must have registered itself with the ROT when it first began running.

<h3><a id="Implementation-specific_Notes"></a><a id="implementation-specific_notes"></a><a id="IMPLEMENTATION-SPECIFIC_NOTES"></a>Implementation-specific Notes</h3>
<table>
<tr>
<th>Implementation</th>
<th>Notes</th>
</tr>
<tr>
<td>Anti-moniker</td>
<td>
This method checks the ROT to see whether the object is running.

</td>
</tr>
<tr>
<td>Class moniker</td>
<td>
This method returns E_NOTIMPL.

</td>
</tr>
<tr>
<td>File moniker</td>
<td>
If <i>pmkNewlyRunning</i> is non-<b>NULL</b>, this method returns <b>TRUE</b> if that moniker is equal to this moniker. Otherwise, the method asks the ROT whether this moniker is running. The method ignores <i>pmkToLeft</i>.

</td>
</tr>
<tr>
<td>Generic composite moniker</td>
<td>
If <i>pmkToLeft</i> is non-<b>NULL</b>, this method composes <i>pmkToLeft</i> with this moniker and calls <b>IsRunning</b> on the result.

If <i>pmkToLeft</i> is <b>NULL</b>, this method returns <b>TRUE</b> if pmkNewlyRunning is non-<b>NULL</b> and is equal to this moniker.

If <i>pmkToLeft</i> and <i>pmkNewlyRunning</i> are both <b>NULL</b>, this method checks the ROT to see whether the moniker is running. If so, the method returns S_OK; otherwise, it recursively calls <b>IsRunning</b> on the rightmost component of the composite, passing the remainder of the composite as the <i>pmkToLeft</i> parameter for that call. This handles the case where the moniker identifies a pseudo-object that is not registered as running; see the item moniker implementation for more details.

</td>
</tr>
<tr>
<td>Item moniker</td>
<td>
If pmkToLeft is <b>NULL</b>, this method returns <b>TRUE</b> if <i>pmkNewlyRunning</i> is non-<b>NULL</b> and is equal to this moniker. Otherwise, the method checks the ROT to see whether this moniker is running.

If pmkToLeft is non-<b>NULL</b>, the method calls <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">IMoniker::BindToObject</a> on the <i>pmkToLeft</i> parameter, requesting an <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleitemcontainer">IOleItemContainer</a> interface pointer. The method then calls <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleitemcontainer-isrunning">IOleItemContainer::IsRunning</a>, passing the string contained within this moniker.

</td>
</tr>
<tr>
<td>OBJREF moniker</td>
<td>
Because OBJREF monikers represent a running object instance, this method returns <b>TRUE</b> unless the object is known to be no longer running because a recent call failed. The method ignores <i>pmkToLeft</i>.

</td>
</tr>
<tr>
<td>Pointer moniker</td>
<td>
This method always returns S_OK, because the object identified by a pointer moniker must always be running.

</td>
</tr>
<tr>
<td>URL moniker</td>
<td>
Returns S_OK if this moniker is currently running. Otherwise, it returns S_FALSE. The URL moniker determines whether it is running by first checking whether it is equal to the newly running moniker, by making the following call: pmkNewlyRunning-&gt;IsEqual. Typically, this call is an inexpensive operation. If this does not succeed, the moniker next checks to see whether it is registered with the ROT of the passed-in bind context.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-bindifrunning">IOleLink::BindIfRunning</a>



<a href="/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-isrunning">IRunningObjectTable::IsRunning</a>