---
UID: NF:objidl.IServerSecurity.RevertToSelf
title: IServerSecurity::RevertToSelf (objidl.h)
description: The IServerSecurity::RevertToSelf method (objidl.h) restores the authentication information of a thread to what it was before impersonation began.
helpviewer_keywords: ["IServerSecurity interface [COM]","RevertToSelf method","IServerSecurity.RevertToSelf","IServerSecurity::RevertToSelf","RevertToSelf","RevertToSelf method [COM]","RevertToSelf method [COM]","IServerSecurity interface","_com_iserversecurity_reverttoself","com.iserversecurity_reverttoself","objidlbase/IServerSecurity::RevertToSelf"]
old-location: com\iserversecurity_reverttoself.htm
tech.root: com
ms.assetid: 21952f54-439e-446f-a206-4b35759b1090
ms.date: 08/15/2022
ms.keywords: IServerSecurity interface [COM],RevertToSelf method, IServerSecurity.RevertToSelf, IServerSecurity::RevertToSelf, RevertToSelf, RevertToSelf method [COM], RevertToSelf method [COM],IServerSecurity interface, _com_iserversecurity_reverttoself, com.iserversecurity_reverttoself, objidlbase/IServerSecurity::RevertToSelf
req.header: objidl.h
req.include-header: ObjIdl.h
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
 - IServerSecurity::RevertToSelf
 - objidl/IServerSecurity::RevertToSelf
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IServerSecurity.RevertToSelf
---

# IServerSecurity::RevertToSelf


## -description

Restores the authentication information of a thread to what it was before impersonation began.



## -returns

If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.

## -remarks

<b>RevertToSelf</b> restores the authentication information on a thread to the authentication information on the thread before impersonation began. If the server does not call <b>RevertToSelf</b> before the end of the current call, it will be called automatically by COM.

When <a href="/windows/desktop/api/objidl/nf-objidl-iserversecurity-impersonateclient">ImpersonateClient</a> is called on a thread that is not currently impersonating, COM saves the token currently on the thread. A subsequent call to <b>RevertToSelf</b> restores the saved token, and <a href="/windows/desktop/api/objidl/nf-objidl-iserversecurity-isimpersonating">IsImpersonating</a> will then return <b>FALSE</b>. This means that if a series of impersonation calls are made using different <a href="/windows/desktop/api/objidl/nn-objidl-iserversecurity">IServerSecurity</a> objects, <b>RevertToSelf</b> will restore the token that was on the thread when the first call to <b>ImpersonateClient</b> was made. Also, only one <b>RevertToSelf</b> call is needed to undo any number of <b>ImpersonateClient</b> calls.

This method will only revert impersonation changes made by <a href="/windows/desktop/api/objidl/nf-objidl-iserversecurity-impersonateclient">ImpersonateClient</a>. If the thread token is modified by other means (through the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadtoken">SetThreadToken</a> or <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient">RpcImpersonateClient</a> functions) the result of this function is undefined.

<b>RevertToSelf</b> affects only the current method invocation. If there are nested method invocations, each invocation can have its own impersonation token and DCOM will correctly restore the impersonation token before returning to them (regardless of whether <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself">CoRevertToSelf</a> or <b>RevertToSelf</b> was called).

It is important to understand that an instance of <a href="/windows/desktop/api/objidl/nn-objidl-iserversecurity">IServerSecurity</a> is valid on any thread in the apartment until the call represented by <b>IServerSecurity</b> completes. However, impersonation is local to a particular thread for the duration of the current call on that thread. Therefore, if two threads in the same apartment use the same <b>IServerSecurity</b> instance to call <a href="/windows/desktop/api/objidl/nf-objidl-iserversecurity-impersonateclient">ImpersonateClient</a>, one thread can call <b>RevertToSelf</b> without affecting the other.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself">CoRevertToSelf</a>



<a href="/windows/desktop/api/objidl/nn-objidl-iserversecurity">IServerSecurity</a>
