---
UID: NF:objidl.IRpcChannelBuffer.SendReceive
title: IRpcChannelBuffer::SendReceive (objidl.h)
description: The IRpcChannelBuffer::SendReceive method (objidl.h) sends a method invocation across an RPC channel to the server stub.
helpviewer_keywords: ["IRpcChannelBuffer interface [COM]","SendReceive method","IRpcChannelBuffer.SendReceive","IRpcChannelBuffer::SendReceive","SendReceive","SendReceive method [COM]","SendReceive method [COM]","IRpcChannelBuffer interface","_com_irpcchannelbuffer_sendreceive","com.irpcchannelbuffer_sendreceive","objidlbase/IRpcChannelBuffer::SendReceive"]
old-location: com\irpcchannelbuffer_sendreceive.htm
tech.root: com
ms.assetid: 8a42fd06-252f-4c1b-bbdb-abc2e3887c46
ms.date: 08/12/2022
ms.keywords: IRpcChannelBuffer interface [COM],SendReceive method, IRpcChannelBuffer.SendReceive, IRpcChannelBuffer::SendReceive, SendReceive, SendReceive method [COM], SendReceive method [COM],IRpcChannelBuffer interface, _com_irpcchannelbuffer_sendreceive, com.irpcchannelbuffer_sendreceive, objidlbase/IRpcChannelBuffer::SendReceive
req.header: objidl.h
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
 - IRpcChannelBuffer::SendReceive
 - objidl/IRpcChannelBuffer::SendReceive
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
 - IRpcChannelBuffer.SendReceive
---

# IRpcChannelBuffer::SendReceive


## -description

Sends a method invocation across an RPC channel to the server stub.

## -parameters

### -param pMessage [in, out]

A pointer to an <a href="/windows/desktop/api/objidl/ns-objidl-rpcolemessage">RPCOLEMESSAGE</a> structure that has been populated with marshaled data.

### -param pStatus [out]

If not <b>NULL</b>, set to 0 on successful execution.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

Before invoking this method, the <a href="/windows/desktop/api/objidl/nf-objidl-irpcchannelbuffer-getbuffer">GetBuffer</a> method must have been invoked to allocate a channel buffer. Upon return, the <b>dataRepresentation</b> buffer of the <a href="/windows/desktop/api/objidl/ns-objidl-rpcolemessage">RPCOLEMESSAGE</a> structure will have been modified to include the data returned by the method invoked on the server. If the invocation was successful, the RPC channel buffer has been freed; otherwise the caller must free it explicitly by calling <a href="/windows/desktop/api/objidl/nf-objidl-irpcchannelbuffer-freebuffer">FreeBuffer</a>.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-irpcchannelbuffer">IRpcChannelBuffer</a>
