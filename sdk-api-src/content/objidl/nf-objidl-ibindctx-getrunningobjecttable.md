---
UID: NF:objidl.IBindCtx.GetRunningObjectTable
title: IBindCtx::GetRunningObjectTable (objidl.h)
description: Retrieves an interface pointer to the running object table (ROT) for the computer on which this bind context is running.
helpviewer_keywords: ["GetRunningObjectTable","GetRunningObjectTable method [COM]","GetRunningObjectTable method [COM]","IBindCtx interface","IBindCtx interface [COM]","GetRunningObjectTable method","IBindCtx.GetRunningObjectTable","IBindCtx::GetRunningObjectTable","_com_ibindctx_getrunningobjecttable","com.ibindctx_getrunningobjecttable","objidl/IBindCtx::GetRunningObjectTable"]
old-location: com\ibindctx_getrunningobjecttable.htm
tech.root: com
ms.assetid: 26938d07-d772-4e72-a6aa-57dd2f2cece1
ms.date: 12/05/2018
ms.keywords: GetRunningObjectTable, GetRunningObjectTable method [COM], GetRunningObjectTable method [COM],IBindCtx interface, IBindCtx interface [COM],GetRunningObjectTable method, IBindCtx.GetRunningObjectTable, IBindCtx::GetRunningObjectTable, _com_ibindctx_getrunningobjecttable, com.ibindctx_getrunningobjecttable, objidl/IBindCtx::GetRunningObjectTable
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
 - IBindCtx::GetRunningObjectTable
 - objidl/IBindCtx::GetRunningObjectTable
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
 - IBindCtx.GetRunningObjectTable
---

# IBindCtx::GetRunningObjectTable


## -description

Retrieves an interface pointer to the running object table (ROT) for the computer on which this bind context is running.

## -parameters

### -param pprot [out]

The address of a <a href="/windows/desktop/api/objidl/nn-objidl-irunningobjecttable">IRunningObjectTable</a>* pointer variable that receives the interface pointer to the running object table. If an error occurs, *<i>pprot</i> is set to <b>NULL</b>. If *<i>pprot</i> is non-<b>NULL</b>, the implementation calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the running table object; it is the caller's responsibility to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>.

## -returns

This method can return the standard return values E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.

## -remarks

The running object table is a globally accessible table on each computer. It keeps track of all the objects that are currently running on the computer.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Typically, those implementing a new moniker class (through an implementation of <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface) call <b>GetRunningObjectTable</b>. It is useful to call this method in an implementation of <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">IMoniker::BindToObject</a> or <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-isrunning">IMoniker::IsRunning</a> to check whether an object is currently running. You can also call this method in the implementation of <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-gettimeoflastchange">IMoniker::GetTimeOfLastChange</a> to learn when a running object was last modified.

Moniker implementations should call this method instead of using the <b>GetRunningObjectTable</b> function. This makes it possible for future implementations of <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> to modify binding behavior.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>



<a href="/windows/desktop/api/objidl/nn-objidl-irunningobjecttable">IRunningObjectTable</a>