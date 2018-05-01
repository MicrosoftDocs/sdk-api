---
UID: NF:objidlbase.IRpcChannelBuffer.GetDestCtx
title: IRpcChannelBuffer::GetDestCtx method
author: windows-driver-content
description: Retrieves the destination context for the RPC channel.
old-location: com\irpcchannelbuffer_getdestctx.htm
old-project: com
ms.assetid: 34599869-0c85-403a-88c2-ea8e865d533a
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: GetDestCtx method [COM], GetDestCtx method [COM], IRpcChannelBuffer interface, GetDestCtx,IRpcChannelBuffer.GetDestCtx, IRpcChannelBuffer, IRpcChannelBuffer interface [COM], GetDestCtx method, IRpcChannelBuffer::GetDestCtx, _com_irpcchannelbuffer_getdestctx, com.irpcchannelbuffer_getdestctx, objidlbase/IRpcChannelBuffer::GetDestCtx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	objidlbase.h
api_name:
-	IRpcChannelBuffer.GetDestCtx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IRpcChannelBuffer::GetDestCtx method


## -description


Retrieves the destination context for the RPC channel.


## -parameters




### -param pdwDestContext [out]

The destination context in which the interface is unmarshaled. Possible values come from the <a href="https://msdn.microsoft.com/d7d09ab2-96e7-48da-9292-0e4ca6cebe64">MSHCTX</a> enumeration.


### -param ppvDestContext [out]

This parameter is reserved and must be <b>NULL</b>.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/1d7d7e1c-a491-4625-97ae-0d4dc5d2fc20">IRpcChannelBuffer</a>
 

 

