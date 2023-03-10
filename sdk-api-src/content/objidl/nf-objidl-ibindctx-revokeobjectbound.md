---
UID: NF:objidl.IBindCtx.RevokeObjectBound
title: IBindCtx::RevokeObjectBound (objidl.h)
description: Removes the object from the bind context, undoing a previous call to RegisterObjectBound.
helpviewer_keywords: ["IBindCtx interface [COM]","RevokeObjectBound method","IBindCtx.RevokeObjectBound","IBindCtx::RevokeObjectBound","RevokeObjectBound","RevokeObjectBound method [COM]","RevokeObjectBound method [COM]","IBindCtx interface","_com_ibindctx_revokeobjectbound","com.ibindctx_revokeobjectbound","objidl/IBindCtx::RevokeObjectBound"]
old-location: com\ibindctx_revokeobjectbound.htm
tech.root: com
ms.assetid: c49421a3-1733-4f54-8e30-d23641f13c38
ms.date: 12/05/2018
ms.keywords: IBindCtx interface [COM],RevokeObjectBound method, IBindCtx.RevokeObjectBound, IBindCtx::RevokeObjectBound, RevokeObjectBound, RevokeObjectBound method [COM], RevokeObjectBound method [COM],IBindCtx interface, _com_ibindctx_revokeobjectbound, com.ibindctx_revokeobjectbound, objidl/IBindCtx::RevokeObjectBound
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
 - IBindCtx::RevokeObjectBound
 - objidl/IBindCtx::RevokeObjectBound
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
 - IBindCtx.RevokeObjectBound
---

# IBindCtx::RevokeObjectBound


## -description

Removes the object from the bind context, undoing a previous call to <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectbound">RegisterObjectBound</a>.

## -parameters

### -param punk [in]

A pointer to the <a href="/windows/desktop/com/iunknown-and-interface-inheritance">IUnknown</a> interface on the object to be removed.

## -returns

This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The object was released successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_NOTBOUND</b></dt>
</dl>
</td>
<td width="60%">
The object was not previously registered.

</td>
</tr>
</table>

## -remarks

You would rarely call this method. It is documented primarily for completeness.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>