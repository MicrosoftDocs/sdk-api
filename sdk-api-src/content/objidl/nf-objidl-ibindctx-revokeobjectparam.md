---
UID: NF:objidl.IBindCtx.RevokeObjectParam
title: IBindCtx::RevokeObjectParam (objidl.h)
description: Removes the specified key and its associated pointer from the bind context's string-keyed table of objects. The key must have previously been inserted into the table with a call to RegisterObjectParam.
helpviewer_keywords: ["IBindCtx interface [COM]","RevokeObjectParam method","IBindCtx.RevokeObjectParam","IBindCtx::RevokeObjectParam","RevokeObjectParam","RevokeObjectParam method [COM]","RevokeObjectParam method [COM]","IBindCtx interface","_com_ibindctx_revokeobjectparam","com.ibindctx_revokeobjectparam","objidl/IBindCtx::RevokeObjectParam"]
old-location: com\ibindctx_revokeobjectparam.htm
tech.root: com
ms.assetid: e7dbf9c8-0ecf-4076-8bec-4da457c60cee
ms.date: 12/05/2018
ms.keywords: IBindCtx interface [COM],RevokeObjectParam method, IBindCtx.RevokeObjectParam, IBindCtx::RevokeObjectParam, RevokeObjectParam, RevokeObjectParam method [COM], RevokeObjectParam method [COM],IBindCtx interface, _com_ibindctx_revokeobjectparam, com.ibindctx_revokeobjectparam, objidl/IBindCtx::RevokeObjectParam
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
 - IBindCtx::RevokeObjectParam
 - objidl/IBindCtx::RevokeObjectParam
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
 - IBindCtx.RevokeObjectParam
---

# IBindCtx::RevokeObjectParam


## -description

Removes the specified key and its associated pointer from the bind context's string-keyed table of objects. The key must have previously been inserted into the table with a call to <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam">RegisterObjectParam</a>.

## -parameters

### -param pszKey [in]

The <a href="/windows/desktop/shell/str-constants">bind context string key</a> to be removed. Key string comparison is case-sensitive.

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
The specified key was removed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The object was not previously registered.

</td>
</tr>
</table>

## -remarks

A bind context maintains a table of interface pointers, each associated with a string key. This enables communication between a moniker implementation and the caller that initiated the binding operation. One party can store an interface pointer under a string known to both parties so that the other party can later retrieve it from the bind context.

This method is used to remove an entry from the table. If the specified key is found, the bind context also releases its reference to the object.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>