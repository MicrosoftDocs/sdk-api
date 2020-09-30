---
UID: NF:objidl.IBindCtx.EnumObjectParam
title: IBindCtx::EnumObjectParam (objidl.h)
description: Retrieves a pointer to an interface that can be used to enumerate the keys of the bind context's string-keyed table of pointers.
helpviewer_keywords: ["EnumObjectParam","EnumObjectParam method [COM]","EnumObjectParam method [COM]","IBindCtx interface","IBindCtx interface [COM]","EnumObjectParam method","IBindCtx.EnumObjectParam","IBindCtx::EnumObjectParam","_com_ibindctx_enumobjectparam","com.ibindctx_enumobjectparam","objidl/IBindCtx::EnumObjectParam"]
old-location: com\ibindctx_enumobjectparam.htm
tech.root: com
ms.assetid: 9e799ce4-e9b3-4b31-98a0-2167a0c19848
ms.date: 12/05/2018
ms.keywords: EnumObjectParam, EnumObjectParam method [COM], EnumObjectParam method [COM],IBindCtx interface, IBindCtx interface [COM],EnumObjectParam method, IBindCtx.EnumObjectParam, IBindCtx::EnumObjectParam, _com_ibindctx_enumobjectparam, com.ibindctx_enumobjectparam, objidl/IBindCtx::EnumObjectParam
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
 - IBindCtx::EnumObjectParam
 - objidl/IBindCtx::EnumObjectParam
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
 - IBindCtx.EnumObjectParam
---

# IBindCtx::EnumObjectParam


## -description

Retrieves a pointer to an interface that can be used to enumerate the keys of the bind context's string-keyed table of pointers.

## -parameters

### -param ppenum [out]

The address of an <a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a>* pointer variable that receives the interface pointer to the enumerator. If an error occurs, *<i>ppenum</i> is set to <b>NULL</b>. If *<i>ppenum</i> is non-<b>NULL</b>, the implementation calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on *<i>ppenum</i>; it is the caller's responsibility to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>.

## -returns

This method can return the standard return values E_OUTOFMEMORY and S_OK.

## -remarks

The keys returned by the enumerator are the ones previously specified in calls to <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam">IBindCtx::RegisterObjectParam</a>.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A bind context maintains a table of interface pointers, each associated with a string key. This enables communication between a moniker implementation and the caller that initiated the binding operation. One party can store an interface pointer under a string known to both parties so that the other party can later retrieve it from the bind context.

In the system implementation of the <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface, this method is not implemented. Therefore, calling this method results in a return value of E_NOTIMPL.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a>