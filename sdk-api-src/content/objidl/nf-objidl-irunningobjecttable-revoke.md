---
UID: NF:objidl.IRunningObjectTable.Revoke
title: IRunningObjectTable::Revoke (objidl.h)
description: Removes an entry from the running object table (ROT) that was previously registered by a call to IRunningObjectTable::Register.
helpviewer_keywords: ["IRunningObjectTable interface [COM]","Revoke method","IRunningObjectTable.Revoke","IRunningObjectTable::Revoke","Revoke","Revoke method [COM]","Revoke method [COM]","IRunningObjectTable interface","_com_irunningobjecttable_revoke","com.irunningobjecttable_revoke","objidl/IRunningObjectTable::Revoke"]
old-location: com\irunningobjecttable_revoke.htm
tech.root: com
ms.assetid: d3d83966-035d-4077-a770-cb62c8011132
ms.date: 12/05/2018
ms.keywords: IRunningObjectTable interface [COM],Revoke method, IRunningObjectTable.Revoke, IRunningObjectTable::Revoke, Revoke, Revoke method [COM], Revoke method [COM],IRunningObjectTable interface, _com_irunningobjecttable_revoke, com.irunningobjecttable_revoke, objidl/IRunningObjectTable::Revoke
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
 - IRunningObjectTable::Revoke
 - objidl/IRunningObjectTable::Revoke
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
 - IRunningObjectTable.Revoke
---

# IRunningObjectTable::Revoke


## -description

Removes an entry from the running object table (ROT) that was previously registered by a call to <a href="/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-register">IRunningObjectTable::Register</a>.

## -parameters

### -param dwRegister [in]

The identifier of the ROT entry to be revoked.

## -returns

This method can return the standard return values E_INVALIDARG and S_OK.

## -remarks

This method undoes the effect of a call to <a href="/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-register">IRunningObjectTable::Register</a>, removing both the moniker and the pointer to the object identified by that moniker.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A moniker provider (hands out monikers identifying its objects to make them accessible to others) must call the <b>Revoke</b> method to revoke the registration of its objects when it stops running. It must have previously called <a href="/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-register">IRunningObjectTable::Register</a> and stored the identifier returned by that method; it uses that identifier when calling <b>Revoke</b>.

The most common type of moniker provider is a compound-document link source. This includes server applications that support linking to their documents (or portions of a document) and container applications that support linking to embeddings within their documents. Server applications that do not support linking can also use the ROT to cooperate with container applications that support linking to embeddings.

If you are writing a container application, you must revoke a document's registration when the document is closed. You must also revoke a document's registration before re-registering it when it is renamed. 



If you are writing a server application, you must revoke an object's registration when the object is closed. You must also revoke an object's registration before re-registering it when its container document is renamed (see <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setmoniker">IOleObject::SetMoniker</a>).

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-irunningobjecttable">IRunningObjectTable</a>