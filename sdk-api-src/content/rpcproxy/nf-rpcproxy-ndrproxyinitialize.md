---
UID: NF:rpcproxy.NdrProxyInitialize
title: NdrProxyInitialize function (rpcproxy.h)
author: windows-sdk-content
description: The NdrProxyInitialize function initializes the proxy for an object method.
old-location: rpc\ndrproxyinitialize.htm
tech.root: Rpc
ms.assetid: 54037337-9166-4023-8470-65ad247ceee5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NdrProxyInitialize, NdrProxyInitialize function [RPC], rpc.ndrproxyinitialize, rpcproxy/NdrProxyInitialize
ms.topic: function
f1_keywords:
- rpcproxy/NdrProxyInitialize
req.header: rpcproxy.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- RpcRT4.dll
api_name:
- NdrProxyInitialize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NdrProxyInitialize function


## -description


The <b>NdrProxyInitialize</b> function initializes the proxy for an object method.


## -parameters




### -param This [in]

Pointer to the interface proxy.


### -param pRpcMsg [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/rpcdcep/ns-rpcdcep-rpc_message">RPC_MESSAGE</a> structure that  contains information about the RPC request. 


### -param pStubMsg [in, out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. Structure is for internal use only; do not modify.


### -param pStubDescriptor [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_desc">MIDL_STUB_DESC</a> structure that contains a descriptor for the RPC stub. Structure is for internal use only; do not modify.


### -param ProcNum [in]

Procedure  number for the object method.


## -returns



This function has no return values. Throws an exception upon error.



