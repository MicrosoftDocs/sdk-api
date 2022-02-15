---
UID: NF:objidl.IRunnableObject.IsRunning
title: IRunnableObject::IsRunning (objidl.h)
description: Determines whether an object is currently in the running state.
helpviewer_keywords: ["IRunnableObject interface [COM]","IsRunning method","IRunnableObject.IsRunning","IRunnableObject::IsRunning","IsRunning","IsRunning method [COM]","IsRunning method [COM]","IRunnableObject interface","_com_irunnableobject_isrunning","com.irunnableobject_isrunning","objidl/IRunnableObject::IsRunning"]
old-location: com\irunnableobject_isrunning.htm
tech.root: com
ms.assetid: 0a4cdd21-8256-4533-9cad-d9e8450a17e9
ms.date: 12/05/2018
ms.keywords: IRunnableObject interface [COM],IsRunning method, IRunnableObject.IsRunning, IRunnableObject::IsRunning, IsRunning, IsRunning method [COM], IsRunning method [COM],IRunnableObject interface, _com_irunnableobject_isrunning, com.irunnableobject_isrunning, objidl/IRunnableObject::IsRunning
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
 - IRunnableObject::IsRunning
 - objidl/IRunnableObject::IsRunning
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
 - IRunnableObject.IsRunning
---

# IRunnableObject::IsRunning


## -description

Determines whether an object is currently in the running state.



## -returns

If the object is in the running state, the return value is <b>TRUE</b>. Otherwise, it is <b>FALSE</b>.

## -remarks

A container application could call <b>IRunnableObject::IsRunning</b> when it needs to know if the server is immediately available. For example, a container's implementation of the <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleitemcontainer-getobject">IOleItemContainer::GetObject</a> method would return an error if the server is not running and the bindspeed parameter specifies BINDSPEED_IMMEDIATE.

An object handler could call <b>IRunnableObject::IsRunning</b> when it wants to avoid conflicts with a running server or when the running server might have more up-to-date information. For example, a handler's implementation of <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getextent">IOleObject::GetExtent</a> would delegate to the object server if it is running, because the server's information might be more current than that in the handler's cache.


<a href="/windows/desktop/api/ole2/nf-ole2-oleisrunning">OleIsRunning</a> is a helper function that conveniently repackages the functionality offered by <b>IRunnableObject::IsRunning</b>. With the release of OLE 2.01, the implementation of <b>OleIsRunning</b> was changed so that it calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a>, asks for <a href="/windows/desktop/api/objidl/nn-objidl-irunnableobject">IRunnableObject</a>, and then calls <b>IRunnableObject::IsRunning</b>. In other words, you can use the interface and the helper function interchangeably.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-irunnableobject">IRunnableObject</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleisrunning">OleIsRunning</a>
