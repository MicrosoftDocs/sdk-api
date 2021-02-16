---
UID: NF:oleidl.IOleItemContainer.GetObjectStorage
title: IOleItemContainer::GetObjectStorage (oleidl.h)
description: Retrieves a pointer to the storage for the specified object.
helpviewer_keywords: ["GetObjectStorage","GetObjectStorage method [COM]","GetObjectStorage method [COM]","IOleItemContainer interface","IOleItemContainer interface [COM]","GetObjectStorage method","IOleItemContainer.GetObjectStorage","IOleItemContainer::GetObjectStorage","_com_ioleitemcontainer_getobjectstorage","com.ioleitemcontainer_getobjectstorage","oleidl/IOleItemContainer::GetObjectStorage"]
old-location: com\ioleitemcontainer_getobjectstorage.htm
tech.root: com
ms.assetid: 13a094bc-bacc-40d5-9682-ecc6072966fa
ms.date: 12/05/2018
ms.keywords: GetObjectStorage, GetObjectStorage method [COM], GetObjectStorage method [COM],IOleItemContainer interface, IOleItemContainer interface [COM],GetObjectStorage method, IOleItemContainer.GetObjectStorage, IOleItemContainer::GetObjectStorage, _com_ioleitemcontainer_getobjectstorage, com.ioleitemcontainer_getobjectstorage, oleidl/IOleItemContainer::GetObjectStorage
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.idl
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
 - IOleItemContainer::GetObjectStorage
 - oleidl/IOleItemContainer::GetObjectStorage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleItemContainer.GetObjectStorage
---

# IOleItemContainer::GetObjectStorage


## -description

Retrieves a pointer to the storage for the specified object.

## -parameters

### -param pszItem [in]

The compound document's name for the object whose storage is requested.

### -param pbc [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface on the bind context to be used in this binding operation. The bind context caches objects bound during the binding process, contains parameters that apply to all operations using the bind context, and provides the means by which the binding implementation should retrieve information about its environment.

### -param riid [in]

A reference to the identifier of the interface to be used to communicate with the object, usually <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>.

### -param ppvStorage [out]

Address of a pointer variable that receives the interface pointer requested in <i>riid</i>. Upon successful return, *<i>ppvStorage</i> contains the requested interface pointer to the storage for the object named by <i>pszItem</i>. When successful, the implementation must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on *<i>ppvStorage</i>; it is the caller's responsibility to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>. If an error occurs, *<i>ppvStorage</i> is set to <b>NULL</b>.

## -returns

This method can return the standard return value E_OUTOFMEMORY, as well as the following values.

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
The method completely successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The parameter <i>pszItem</i> does not identify a object in this container.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_NOSTORAGE</b></dt>
</dl>
</td>
<td width="60%">
The object does not have its own independent storage.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The requested interface is not available.

</td>
</tr>
</table>

## -remarks

The item moniker implementation of <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtostorage">IMoniker::BindToStorage</a> calls this method.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If <i>pszItem</i> designates a pseudo-object, your implementation of <b>IOleItemContainer::GetObjectStorage</b> should return MK_E_NOSTORAGE, because pseudo-objects do not have their own independent storage. If <i>pszItem</i> designates an embedded object, or a portion of the document that has its own storage, your implementation should return the specified interface pointer on the appropriate storage object.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleitemcontainer">IOleItemContainer</a>