---
UID: NF:objidl.IBindCtx.GetObjectParam
title: IBindCtx::GetObjectParam (objidl.h)
description: Retrieves an interface pointer to the object associated with the specified key in the bind context's string-keyed table of pointers.
helpviewer_keywords: ["GetObjectParam","GetObjectParam method [COM]","GetObjectParam method [COM]","IBindCtx interface","IBindCtx interface [COM]","GetObjectParam method","IBindCtx.GetObjectParam","IBindCtx::GetObjectParam","_com_ibindctx_getobjectparam","com.ibindctx_getobjectparam","objidl/IBindCtx::GetObjectParam"]
old-location: com\ibindctx_getobjectparam.htm
tech.root: com
ms.assetid: 8f423495-7a34-4901-968e-1fe204680d8a
ms.date: 12/05/2018
ms.keywords: GetObjectParam, GetObjectParam method [COM], GetObjectParam method [COM],IBindCtx interface, IBindCtx interface [COM],GetObjectParam method, IBindCtx.GetObjectParam, IBindCtx::GetObjectParam, _com_ibindctx_getobjectparam, com.ibindctx_getobjectparam, objidl/IBindCtx::GetObjectParam
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
 - IBindCtx::GetObjectParam
 - objidl/IBindCtx::GetObjectParam
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
 - IBindCtx.GetObjectParam
---

# IBindCtx::GetObjectParam


## -description

Retrieves an interface pointer to the object associated with the specified key in the bind context's string-keyed table of pointers.

## -parameters

### -param pszKey [in]

The <a href="/windows/desktop/shell/str-constants">bind context string key</a> to be searched for. Key string comparison is case-sensitive.

### -param ppunk [out]

The address of an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>* pointer variable that receives the interface pointer to the object associated with <i>pszKey</i>. When successful, the implementation calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on *<i>ppunk</i>. It is the caller's responsibility to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>. If an error occurs, the implementation sets *<i>ppunk</i> to <b>NULL</b>.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.

## -remarks

A bind context maintains a table of interface pointers, each associated with a string key. This enables communication between a moniker implementation and the caller that initiated the binding operation. One party can store an interface pointer under a string known to both parties so that the other party can later retrieve it from the bind context.

The pointer this method retrieves must have previously been inserted into the table using the <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam">IBindCtx::RegisterObjectParam</a> method.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Objects using monikers to locate other objects can call this method when a binding operation fails to get specific information about the error that occurred. Depending on the error, it may be possible to correct the situation and retry the binding operation. See <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam">IBindCtx::RegisterObjectParam</a> for more information.

Moniker implementations can call this method to handle situations where a caller initiates a binding operation and requests specific information. By convention, the implementer should use key names that begin with the string form of the CLSID of a moniker class. (See the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-stringfromclsid">StringFromCLSID</a> function.)

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>