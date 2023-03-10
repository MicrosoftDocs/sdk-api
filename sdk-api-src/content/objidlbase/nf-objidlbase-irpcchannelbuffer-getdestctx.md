---
UID: NF:objidlbase.IRpcChannelBuffer.GetDestCtx
title: IRpcChannelBuffer::GetDestCtx (objidlbase.h)
description: The IRpcChannelBuffer::GetDestCtx (objidlbase.h) method retrieves the destination context for the RPC channel.
helpviewer_keywords: ["GetDestCtx","GetDestCtx method [COM]","GetDestCtx method [COM]","IRpcChannelBuffer interface","IRpcChannelBuffer interface [COM]","GetDestCtx method","IRpcChannelBuffer.GetDestCtx","IRpcChannelBuffer::GetDestCtx","_com_irpcchannelbuffer_getdestctx","com.irpcchannelbuffer_getdestctx","objidlbase/IRpcChannelBuffer::GetDestCtx"]
old-location: com\irpcchannelbuffer_getdestctx.htm
tech.root: com
ms.assetid: 34599869-0c85-403a-88c2-ea8e865d533a
ms.date: 08/13/2022
ms.keywords: GetDestCtx, GetDestCtx method [COM], GetDestCtx method [COM],IRpcChannelBuffer interface, IRpcChannelBuffer interface [COM],GetDestCtx method, IRpcChannelBuffer.GetDestCtx, IRpcChannelBuffer::GetDestCtx, _com_irpcchannelbuffer_getdestctx, com.irpcchannelbuffer_getdestctx, objidlbase/IRpcChannelBuffer::GetDestCtx
req.header: objidlbase.h
req.include-header: ObjIdl.h
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
 - IRpcChannelBuffer::GetDestCtx
 - objidlbase/IRpcChannelBuffer::GetDestCtx
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
 - IRpcChannelBuffer.GetDestCtx
---

# IRpcChannelBuffer::GetDestCtx


## -description

Retrieves the destination context for the RPC channel.

## -parameters

### -param pdwDestContext [out]

The destination context in which the interface is unmarshaled. Possible values come from the <a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-mshctx">MSHCTX</a> enumeration.

### -param ppvDestContext [out]

This parameter is reserved and must be <b>NULL</b>.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-irpcchannelbuffer">IRpcChannelBuffer</a>
