---
UID: NF:objidl.IRunnableObject.Run
title: IRunnableObject::Run (objidl.h)
description: Forces an object to run.
helpviewer_keywords: ["IRunnableObject interface [COM]","Run method","IRunnableObject.Run","IRunnableObject::Run","Run","Run method [COM]","Run method [COM]","IRunnableObject interface","_com_irunnableobject_run","com.irunnableobject_run","objidl/IRunnableObject::Run"]
old-location: com\irunnableobject_run.htm
tech.root: com
ms.assetid: fb79e81c-0655-48ea-afb5-dab3529676d0
ms.date: 12/05/2018
ms.keywords: IRunnableObject interface [COM],Run method, IRunnableObject.Run, IRunnableObject::Run, Run, Run method [COM], Run method [COM],IRunnableObject interface, _com_irunnableobject_run, com.irunnableobject_run, objidl/IRunnableObject::Run
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
 - IRunnableObject::Run
 - objidl/IRunnableObject::Run
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
 - IRunnableObject.Run
---

# IRunnableObject::Run


## -description

Forces an object to run.

## -parameters

### -param pbc [in]

A pointer to the binding context of the run operation. See <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>. This parameter can be <b>NULL</b>.

## -returns

This method can return the standard return values E_INVALIDARG, E_UNEXPECTED, and S_OK.

## -remarks

Containers call <b>IRunnableObject::Run</b> to force their objects to enter the running state. If the object is not already running, calling <b>Run</b> can be an expensive operation, on the order of many seconds. If the object is already running, then this method has no effect on the object.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
When called on a linked object that has been converted to a new class since the link was last activated, <b>IRunnableObject::Run</b> may return OLE_E_CLASSDIFF. In this case, the client should call <a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-bindtosource">IOleLink::BindToSource</a>.


<a href="/windows/desktop/api/ole2/nf-ole2-olerun">OleRun</a> is a helper function that conveniently repackages the functionality offered by <b>IRunnableObject::Run</b>. With the release of OLE 2.01, the implementation of <b>OleRun</b> was changed so that it calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a>, asks for <a href="/windows/desktop/api/objidl/nn-objidl-irunnableobject">IRunnableObject</a>, and then calls <b>IRunnableObject::Run</b>. In other words, you can use the interface and the helper function interchangeably.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The object should register in the running object table if it has a moniker assigned. The object should not hold any strong locks on itself; instead, it should remain in the unstable, unlocked state. The object should be locked when the first external connection is made to the object.

An embedded object must hold a lock on its embedding container while it is in the running state. The default handler provided by OLE 2 takes care of locking the embedding container on behalf of objects implemented by an EXE object application. Objects implemented by a DLL object application must explicitly put a lock on their embedding containers, which they do by first calling <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-getcontainer">IOleClientSite::GetContainer</a> to get a pointer to the container, then calling <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecontainer-lockcontainer">IOleContainer::LockContainer</a> to actually place the lock. This lock must be released when <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-close">IOleObject::Close</a> is called.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-irunnableobject">IRunnableObject</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olerun">OleRun</a>