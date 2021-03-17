---
UID: NF:objidl.IRunningObjectTable.Register
title: IRunningObjectTable::Register (objidl.h)
description: Registers an object and its identifying moniker in the running object table (ROT).
helpviewer_keywords: ["IRunningObjectTable interface [COM]","Register method","IRunningObjectTable.Register","IRunningObjectTable::Register","ROTFLAGS_ALLOWANYCLIENT","ROTFLAGS_REGISTRATIONKEEPSALIVE","Register","Register method [COM]","Register method [COM]","IRunningObjectTable interface","_com_irunningobjecttable_register","com.irunningobjecttable_register","objidl/IRunningObjectTable::Register"]
old-location: com\irunningobjecttable_register.htm
tech.root: com
ms.assetid: 40f815b2-dfea-416c-aae1-7ba3a710ad91
ms.date: 12/05/2018
ms.keywords: IRunningObjectTable interface [COM],Register method, IRunningObjectTable.Register, IRunningObjectTable::Register, ROTFLAGS_ALLOWANYCLIENT, ROTFLAGS_REGISTRATIONKEEPSALIVE, Register, Register method [COM], Register method [COM],IRunningObjectTable interface, _com_irunningobjecttable_register, com.irunningobjecttable_register, objidl/IRunningObjectTable::Register
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
 - IRunningObjectTable::Register
 - objidl/IRunningObjectTable::Register
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
 - IRunningObjectTable.Register
---

# IRunningObjectTable::Register


## -description

Registers an object and its identifying moniker in the running object table (ROT).

## -parameters

### -param grfFlags [in]

Specifies whether the ROT's reference to punkObject is weak or strong and controls access to the object through its entry in the ROT. For details, see the Remarks section.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ROTFLAGS_REGISTRATIONKEEPSALIVE"></a><a id="rotflags_registrationkeepsalive"></a><dl>
<dt><b>ROTFLAGS_REGISTRATIONKEEPSALIVE</b></dt>
</dl>
</td>
<td width="60%">
When set, indicates a strong registration for the object. 

</td>
</tr>
<tr>
<td width="40%"><a id="ROTFLAGS_ALLOWANYCLIENT"></a><a id="rotflags_allowanyclient"></a><dl>
<dt><b>ROTFLAGS_ALLOWANYCLIENT</b></dt>
</dl>
</td>
<td width="60%">
When set, any client can connect to the running object through its entry in the ROT. When not set, only clients in the window station that registered the object can connect to it.

</td>
</tr>
</table>

### -param punkObject [in]

A pointer to the object that is being registered as running.

### -param pmkObjectName [in]

A pointer to the moniker that identifies <i>punkObject</i>.

### -param pdwRegister [out]

An identifier for this ROT entry that can be used in subsequent calls to <a href="/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-revoke">IRunningObjectTable::Revoke</a> or <a href="/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-notechangetime">IRunningObjectTable::NoteChangeTime</a>. The caller cannot specify <b>NULL</b> for this parameter. If an error occurs, *<i>pdwRegister</i> is set to zero.

## -returns

This method can return the standard return values E_INVALIDARG and E_OUTOFMEMORY, as well as the following values.

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
<dt><b>MK_S_MONIKERALREADYREGISTERED</b></dt>
</dl>
</td>
<td width="60%">
The moniker/object pair was successfully registered, but that another object (possibly the same object) has already been registered with the same moniker.

</td>
</tr>
</table>

## -remarks

This method registers a pointer to an object under a moniker that identifies the object. The moniker is used as the key when the table is searched with <a href="/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-getobject">IRunningObjectTable::GetObject</a>.

When an object is registered, the ROT always calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the object. For a weak registration (ROTFLAGS_REGISTRATIONKEEPSALIVE not set), the ROT will release the object whenever the last strong reference to the object is released. For a strong registration (ROTFLAGS_REGISTRATIONKEEPSALIVE set), the ROT prevents the object from being destroyed until the object's registration is explicitly revoked.

A server registered as either LocalService or RunAs can set the ROTFLAGS_ALLOWANYCLIENT flag in its call to <b>Register</b> to allow any client to connect to it. A server setting this bit must have its executable name in the AppID section of the registry that refers to the AppID for the executable. An "activate as activator" server (not registered as LocalService or RunAs) must not set this flag in its call to <b>Register</b>. For details on installing services, see <a href="/windows/desktop/com/installing-as-a-service-application">Installing as a Service Application</a>.

Registering a second object with the same moniker, or re-registering the same object with the same moniker, creates a second entry in the ROT. In this case, <b>Register</b> returns MK_S_MONIKERALREADYREGISTERED. Each call to <b>Register</b> must be matched by a call to <a href="/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-revoke">IRunningObjectTable::Revoke</a> because even duplicate entries have different <i>pdwRegister</i> identifiers. A problem with duplicate registrations is that there is no way to determine which object will be returned if the moniker is specified in a subsequent call to <a href="/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-isrunning">IRunningObjectTable::IsRunning</a>.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
If you are a moniker provider (that is, you hand out monikers identifying your objects to make them accessible to others), you must call the <b>Register</b> method to register your objects when they begin running. You must also call this method if you rename your objects while they are loaded. 



The most common type of moniker provider is a compound-document link source. This includes server applications that support linking to their documents (or portions of a document) and container applications that support linking to embeddings within their documents. Server applications that do not support linking can also use the ROT to cooperate with container applications that support linking to embeddings.



If you are writing a server application, you should register an object with the ROT when it begins running, typically in your implementation of <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-doverb">IOleObject::DoVerb</a>. The object must be registered under its full moniker, which requires getting the moniker of its container document using <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-getmoniker">IOleClientSite::GetMoniker</a>. You should also revoke and re-register the object in your implementation of <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setmoniker">IOleObject::SetMoniker</a>, which is called if the container document is renamed.

If you are writing a container application that supports linking to embeddings, you should register your document with the ROT when it is loaded. If your document is renamed, you should revoke and re-register it with the ROT and call <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setmoniker">IOleObject::SetMoniker</a> for any embedded objects in the document to give them an opportunity to re-register themselves.

Objects registered in the ROT must be explicitly revoked when the object is no longer running or when its moniker changes. This revocation is important because there is no way for the system to automatically remove entries from the ROT. You must cache the identifier that is written through pdwRegister and use it in a call to <a href="/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-revoke">IRunningObjectTable::Revoke</a> to revoke the registration. For a strong registration, a strong reference is released when the objects registration is revoked.

As of Windows Server 2003, if there are stale entries that remain in the ROT due to unexpected server problems, COM will automatically remove these stale entries from the ROT.

The system's implementation of <b>Register</b> calls <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-reduce">IMoniker::Reduce</a> on the <i>pmkObjectName</i> parameter to ensure that the moniker is fully reduced before registration. If an object is known by more than one fully reduced moniker, it should be registered under all such monikers.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-irunningobjecttable">IRunningObjectTable</a>