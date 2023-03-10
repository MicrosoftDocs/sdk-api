---
UID: NF:unknwn.IClassFactory.LockServer
title: IClassFactory::LockServer
description: The IClassFactory::LockServer method locks an object application open in memory. This enables instances to be created more quickly.
helpviewer_keywords: ["IClassFactory interface [COM]","LockServer method","IClassFactory.LockServer","IClassFactory::LockServer","LockServer","LockServer method [COM]","LockServer method [COM]","IClassFactory interface","_com_iclassfactory_lockserver","com.iclassfactory_lockserver","unknwnbase/IClassFactory::LockServer"]
old-location: com\iclassfactory_lockserver.htm
tech.root: com
ms.assetid: 4c817b89-013d-477f-a713-5e320896dfa0
ms.date: 08/15/2022
ms.keywords: IClassFactory interface [COM],LockServer method, IClassFactory.LockServer, IClassFactory::LockServer, LockServer, LockServer method [COM], LockServer method [COM],IClassFactory interface, _com_iclassfactory_lockserver, com.iclassfactory_lockserver, unknwnbase/IClassFactory::LockServer
req.header: unknwn.h
req.include-header: Unknwn.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Unknwn.idl
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
 - IClassFactory::LockServer
 - unknwn/IClassFactory::LockServer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - unknwnbase.h
api_name:
 - IClassFactory.LockServer
---

## -description

Locks an object application open in memory. This enables instances to be created more quickly.

## -parameters

### -param fLock [in]

If <b>TRUE</b>, increments the lock count; if <b>FALSE</b>, decrements the lock count.

## -returns

This method can return the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

<b>IClassFactory::LockServer</b> controls whether an object's server is kept in memory. Keeping the application alive in memory allows instances to be created more quickly.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Most clients do not need to call this method. It is provided only for those clients that require special performance in creating multiple instances of their objects.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If the lock count is zero, there are no more objects in use, and the application is not under user control, the server can be closed. One way to implement <b>LockServer</b> is to call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-colockobjectexternal">CoLockObjectExternal</a> function.

The process that locks the object application is responsible for unlocking it. After the class object is released, there is no mechanism that guarantees the caller connection to the same class later (as in the case where a class object is registered as single-use). It is important to count all calls, not just the last one, to <b>LockServer</b>, because calls must be balanced before attempting to release the pointer to the <a href="/windows/desktop/api/unknwnbase/nn-unknwnbase-iclassfactory">IClassFactory</a> interface on the class object or an error results. For every call to <b>LockServer</b> with <i>fLock</i> set to <b>TRUE</b>, there must be a call to <b>LockServer</b> with <i>fLock</i> set to <b>FALSE</b>. When the lock count and the class object reference count are both zero, the class object can be freed.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-colockobjectexternal">CoLockObjectExternal</a>

<a href="/windows/desktop/api/unknwnbase/nn-unknwnbase-iclassfactory">IClassFactory</a>
