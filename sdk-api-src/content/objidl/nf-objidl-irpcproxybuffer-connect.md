---
UID: NF:objidl.IRpcProxyBuffer.Connect
title: IRpcProxyBuffer::Connect
author: windows-sdk-content
description: Initializes a client proxy, binding it to the specified RPC channel.
old-location: com\irpcproxybuffer_connect.htm
old-project: com
ms.assetid: 18651110-9d20-4acc-b21e-9a93099e31bd
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: Connect, Connect method [COM], Connect method [COM],IRpcProxyBuffer interface, IRpcProxyBuffer interface [COM],Connect method, IRpcProxyBuffer.Connect, IRpcProxyBuffer::Connect, _com_irpcproxybuffer_connect, com.irpcproxybuffer_connect, objidlbase/IRpcProxyBuffer::Connect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	objidlbase.h
api_name:
-	IRpcProxyBuffer.Connect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRpcProxyBuffer::Connect


## -description


Initializes a client proxy, binding it to the specified RPC channel.


## -parameters




### -param pRpcChannelBuffer [in]

A pointer to the <a href="https://msdn.microsoft.com/1d7d7e1c-a491-4625-97ae-0d4dc5d2fc20">IRpcChannelBuffer</a> interface that the proxy uses to marshal data.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/e1b18997-f99b-4611-8ba6-da28fd8df898">IRpcProxyBuffer</a>
 

 

