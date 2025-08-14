---
UID: NF:combaseapi.CoLockObjectExternal
title: CoLockObjectExternal function (combaseapi.h)
description: Called either to lock an object to ensure that it stays in memory, or to release such a lock.
helpviewer_keywords: ["CoLockObjectExternal","CoLockObjectExternal function [COM]","_com_CoLockObjectExternal","com.colockobjectexternal","combaseapi/CoLockObjectExternal"]
old-location: com\colockobjectexternal.htm
tech.root: com
ms.assetid: 36eb55f1-06de-49ad-8a8d-91693ca92e99
ms.date: 12/05/2018
ms.keywords: CoLockObjectExternal, CoLockObjectExternal function [COM], _com_CoLockObjectExternal, com.colockobjectexternal, combaseapi/CoLockObjectExternal
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoLockObjectExternal
 - combaseapi/CoLockObjectExternal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-ole32-l1-1-0.dll
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoLockObjectExternal
---

# CoLockObjectExternal function


## -description

Called either to lock an object to ensure that it stays in memory, or to release such a lock.

## -parameters

### -param pUnk [in]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on the object to be locked or unlocked.

### -param fLock [in]

Indicates whether the object is to be locked or released. If this parameter is <b>TRUE</b>, the object is kept in memory, independent of <b>AddRef</b>/<b>Release</b> operations, registrations, or revocations. If this parameter is <b>FALSE</b>, the lock previously set with a call to this function is released.

### -param fLastUnlockReleases [in]

If the lock is the last reference that is supposed to keep an object alive, specify <b>TRUE</b> to release all pointers to the object (there may be other references that are not supposed to keep it alive).
Otherwise, specify <b>FALSE</b>.

If <i>fLock</i> is <b>TRUE</b>, this parameter is ignored.

## -returns

This function can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.

## -remarks

The <b>CoLockObjectExternal</b> function must be called in the process in which the object actually resides (the EXE process, not the process in which handlers may be loaded). 



The <b>CoLockObjectExternal</b> function prevents the reference count of an object from going to zero, thereby "locking" it into existence until the lock is released. The same function (with different parameters) releases the lock. The lock is implemented by having the system call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> on the object. The system then waits to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> on the object until a later call to <b>CoLockObjectExternal</b> with <i>fLock</i> set to <b>FALSE</b>. This function can be used to maintain a reference count on the object on behalf of the end user, because it acts outside of the object, as does the user.

The end user has explicit control over the lifetime of an application, even if there are external locks on it. That is, if a user decides to close the application, it must shut down. In the presence of external locks (such as the lock set by <b>CoLockObjectExternal</b>), the application can call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-codisconnectobject">CoDisconnectObject</a> function to force these connections to close prior to shutdown.


Calling <b>CoLockObjectExternal</b> sets a strong lock on an object. A strong lock keeps an object in memory, while a weak lock does not. Strong locks are required, for example, during a silent update to an OLE embedding. The embedded object's container must remain in memory until the update process is complete. There must also be a strong lock on an application object to ensure that the application stays alive until it has finished providing services to its clients. All external references place a strong reference lock on an object.



The <b>CoLockObjectExternal</b> function is typically called in the following situations: 

<ul>
<li>
Object servers should call <b>CoLockObjectExternal</b> with both <i>fLock</i> and <i>fLastLockReleases</i> set to <b>TRUE</b> when they become visible. This call creates a strong lock on behalf of the user. When the application is closing, free the lock with a call to <b>CoLockObjectExternal</b>, setting <i>fLock</i> to <b>FALSE</b> and <i>fLastLockReleases</i> to <b>TRUE</b>.

</li>
<li>
A call to <b>CoLockObjectExternal</b> on the server can also be used in the implementation of <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecontainer-lockcontainer">IOleContainer::LockContainer</a>.

</li>
</ul>
There are several things to be aware of when you use <b>CoLockObjectExternal</b> in the implementation of <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecontainer-lockcontainer">LockContainer</a>. An embedded object would call <b>LockContainer</b> on its container to keep it running (to lock it) in the absence of other reasons to keep it running. When the embedded object becomes visible, the container must weaken its connection to the embedded object with a call to the <a href="/windows/desktop/api/ole2/nf-ole2-olesetcontainedobject">OleSetContainedObject</a> function, so other connections can affect the object.



Unless an application manages all aspects of its application and document shutdown completely with calls to <b>CoLockObjectExternal</b>, the container must keep a private lock count in <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecontainer-lockcontainer">LockContainer</a> so that it exits when the lock count reaches zero and the container is invisible. Maintaining all aspects of shutdown, and thereby avoiding keeping a private lock count, means that <b>CoLockObjectExternal</b> should be called whenever one of the following conditions occur: 



<ul>
<li>
A document is created and destroyed or made visible or invisible.

</li>
<li>
An application is started and shut down by the user.

</li>
<li>
A pseudo-object is created and destroyed.

</li>
</ul>
For debugging purposes, it may be useful to keep a count of the number of external locks (and unlocks) set on the application.

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-iolecontainer-lockcontainer">IOleContainer::LockContainer</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olesetcontainedobject">OleSetContainedObject</a>