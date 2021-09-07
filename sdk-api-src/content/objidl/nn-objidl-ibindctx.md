---
UID: NN:objidl.IBindCtx
title: IBindCtx (objidl.h)
description: Provides access to a bind context, which is an object that stores information about a particular moniker binding operation.
helpviewer_keywords: ["IBindCtx","IBindCtx interface [COM]","IBindCtx interface [COM]","described","_com_ibindctx","com.ibindctx","objidl/IBindCtx"]
old-location: com\ibindctx.htm
tech.root: com
ms.assetid: e4c8abb5-0c89-44dd-8d95-efbfcc999b46
ms.date: 12/05/2018
ms.keywords: IBindCtx, IBindCtx interface [COM], IBindCtx interface [COM],described, _com_ibindctx, com.ibindctx, objidl/IBindCtx
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
 - IBindCtx
 - objidl/IBindCtx
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
 - IBindCtx
---

# IBindCtx interface


## -description

Provides access to a bind context, which is an object that stores information about a particular moniker binding operation.

## -inheritance

The <b>IBindCtx</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBindCtx</b> also has these types of members:

## -remarks

A bind context includes the following information:

<ul>
<li>A <a href="/windows/desktop/api/objidl/ns-objidl-bind_opts">BIND_OPTS</a> structure containing a set of parameters that do not change during the binding operation. When a composite moniker is bound, each component uses the same bind context, so it acts as a mechanism for passing the same parameters to each component of a composite moniker. 
</li>
<li>A set of pointers to objects that the binding operation has activated. The bind context holds pointers to these bound objects, keeping them loaded and thus eliminating redundant activations if the objects are needed again during subsequent binding operations.</li>
<li>A pointer to the running object table (ROT) on the same computer as the process that started the bind operation. Moniker implementations that need to access the ROT should use the <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getrunningobjecttable">IBindCtx::GetRunningObjectTable</a> method rather than using the <a href="/windows/desktop/api/objbase/nf-objbase-getrunningobjecttable">GetRunningObjectTable</a> function. This allows future enhancements to the system's <b>IBindCtx</b> implementation to modify binding behavior.
</li>
<li>A table of interface pointers, each associated with a string key. This capability enables moniker implementations to store interface pointers under a well-known string so that they can later be retrieved from the bind context. For example, OLE defines several string keys ("ExceededDeadline", "ConnectManually", and so on) that can be used to store a pointer to the object that caused an error during a binding operation.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-createbindctx">CreateBindCtx</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleitemcontainer">IOleItemContainer</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iparsedisplayname">IParseDisplayName</a>
