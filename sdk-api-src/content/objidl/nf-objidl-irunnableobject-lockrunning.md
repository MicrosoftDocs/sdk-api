---
UID: NF:objidl.IRunnableObject.LockRunning
title: IRunnableObject::LockRunning (objidl.h)
description: Locks an already running object into its running state or unlocks it from its running state. (IRunnableObject.LockRunning)
helpviewer_keywords: ["IRunnableObject interface [COM]","LockRunning method","IRunnableObject.LockRunning","IRunnableObject::LockRunning","LockRunning","LockRunning method [COM]","LockRunning method [COM]","IRunnableObject interface","_com_irunnableobject_lockrunning","com.irunnableobject_lockrunning","objidl/IRunnableObject::LockRunning"]
old-location: com\irunnableobject_lockrunning.htm
tech.root: com
ms.assetid: ce501785-16ad-4120-abea-41e2d6ca67df
ms.date: 12/05/2018
ms.keywords: IRunnableObject interface [COM],LockRunning method, IRunnableObject.LockRunning, IRunnableObject::LockRunning, LockRunning, LockRunning method [COM], LockRunning method [COM],IRunnableObject interface, _com_irunnableobject_lockrunning, com.irunnableobject_lockrunning, objidl/IRunnableObject::LockRunning
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
 - IRunnableObject::LockRunning
 - objidl/IRunnableObject::LockRunning
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
 - IRunnableObject.LockRunning
---

# IRunnableObject::LockRunning


## -description

Locks an already running object into its running state or unlocks it from its running state.

## -parameters

### -param fLock [in]

<b>TRUE</b> locks the object into its running state. <b>FALSE</b> unlocks the object from its running state.

### -param fLastUnlockCloses [in]

<b>TRUE</b> specifies that if the connection being released is the last external lock on the object, the object should close. <b>FALSE</b> specifies that the object should remain open until closed by the user or another process.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

Most implementations of <b>IRunnableObject::LockRunning</b> call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-colockobjectexternal">CoLockObjectExternal</a>.


<a href="/windows/desktop/api/ole2/nf-ole2-olelockrunning">OleLockRunning</a> is a helper function that conveniently repackages the functionality offered by <b>IRunnableObject::LockRunning</b>. With the release of OLE 2.01, the implementation of <b>OleLockRunning</b> was changed to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a>, ask for <a href="/windows/desktop/api/objidl/nn-objidl-irunnableobject">IRunnableObject</a>, and then call <b>IRunnableObject::LockRunning</b>. In other words, you can use the interface and the helper function interchangeably.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-colockobjectexternal">CoLockObjectExternal</a>



<a href="/windows/desktop/api/objidl/nn-objidl-irunnableobject">IRunnableObject</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olelockrunning">OleLockRunning</a>
