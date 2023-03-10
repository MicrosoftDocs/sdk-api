---
UID: NF:objidl.IBindCtx.RegisterObjectParam
title: IBindCtx::RegisterObjectParam (objidl.h)
description: Associates an object with a string key in the bind context's string-keyed table of pointers.
helpviewer_keywords: ["IBindCtx interface [COM]","RegisterObjectParam method","IBindCtx.RegisterObjectParam","IBindCtx::RegisterObjectParam","RegisterObjectParam","RegisterObjectParam method [COM]","RegisterObjectParam method [COM]","IBindCtx interface","_com_ibindctx_registerobjectparam","com.ibindctx_registerobjectparam","objidl/IBindCtx::RegisterObjectParam"]
old-location: com\ibindctx_registerobjectparam.htm
tech.root: com
ms.assetid: 7ee2b5b2-9b9c-41f1-8e58-7432ebc0f9ed
ms.date: 12/05/2018
ms.keywords: IBindCtx interface [COM],RegisterObjectParam method, IBindCtx.RegisterObjectParam, IBindCtx::RegisterObjectParam, RegisterObjectParam, RegisterObjectParam method [COM], RegisterObjectParam method [COM],IBindCtx interface, _com_ibindctx_registerobjectparam, com.ibindctx_registerobjectparam, objidl/IBindCtx::RegisterObjectParam
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - IBindCtx::RegisterObjectParam
 - objidl/IBindCtx::RegisterObjectParam
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
 - IBindCtx.RegisterObjectParam
---

# IBindCtx::RegisterObjectParam


## -description

Associates an object with a string key in the bind context's string-keyed table of pointers.

## -parameters

### -param pszKey [in]

The <a href="/windows/desktop/shell/str-constants">bind context string key</a> under which the object is being registered. Key string comparison is case-sensitive.

### -param punk [in]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on the object that is to be registered.

The method calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the pointer.

## -returns

This method can return the standard return values E_OUTOFMEMORY and S_OK.

## -remarks

A bind context maintains a table of interface pointers, each associated with a string key. This enables communication between a moniker implementation and the caller that initiated the binding operation. One party can store an interface pointer under a string known to both parties so that the other party can later retrieve it from the bind context.

Binding operations subsequent to the use of this method can use <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam">IBindCtx::GetObjectParam</a> to retrieve the stored pointer.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
<b>RegisterObjectParam</b> is useful to those implementing a new moniker class (through an implementation of <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>) and to moniker clients (those who use monikers to bind to objects).

In implementing a new moniker class, you call this method when an error occurs during moniker binding to inform the caller of the cause of the error. The key that you would obtain with a call to this method would depend on the error condition. Following is a list of common moniker binding errors, describing for each the keys that would be appropriate:

<ul>
<li>MK_E_EXCEEDEDDEADLINE: If a binding operation exceeds its deadline because a given object is not running, you should register the object's moniker using the first unused key from the list: "ExceededDeadline", "ExceededDeadline1", "ExceededDeadline2", and so on. If the caller later finds the moniker in the running object table, the caller can retry the binding operation.</li>
<li>MK_E_CONNECTMANUALLY: The "ConnectManually" key indicates a moniker whose binding requires assistance from the end user. To request that the end user manually connect to the object, the caller can retry the binding operation after showing the moniker's display name. Common reasons for this error are that a password is needed or that a floppy needs to be mounted.</li>
<li>E_CLASSNOTFOUND: The "ClassNotFound" key indicates a moniker whose class could not be found. (The server for the object identified by this moniker could not be located.) If this key is used for an OLE compound-document object, the caller can use <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtostorage">IMoniker::BindToStorage</a> to bind to the object and then try to carry out a <b>Treat As...</b> or <b>Convert To...</b> operation to associate the object with a different server. If this is successful, the caller can retry the binding operation.</li>
</ul>
A moniker client with detailed knowledge of the implementation of the moniker can also call this method to pass private information to that implementation.

You can define new strings as keys for storing pointers. By convention, you should use key names that begin with the string form of the CLSID of the moniker class. (See the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-stringfromclsid">StringFromCLSID</a> function.)

If the <i>pszKey</i> parameter matches the name of an existing key in the bind context's table, the new object replaces the existing object in the table.

When you register an object using this method, the object is not released until one of the following occurs:

<ul>
<li>It is replaced in the table by another object with the same key.</li>
<li>It is removed from the table by a call to <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-revokeobjectparam">IBindCtx::RevokeObjectParam</a>.</li>
<li>The bind context is released. All registered objects are released when the bind context is released.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>