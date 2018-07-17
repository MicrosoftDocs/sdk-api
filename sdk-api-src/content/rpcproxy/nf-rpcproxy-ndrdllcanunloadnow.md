---
UID: NF:rpcproxy.NdrDllCanUnloadNow
title: NdrDllCanUnloadNow function
author: windows-sdk-content
description: The NdrDllCanUnloadNow function determines whether the DLL that implements the proxy and stub is still in use. If not, the caller can safely unload the DLL from memory.
old-location: rpc\ndrdllcanunloadnow.htm
old-project: rpc
ms.assetid: 25cc5909-87f7-4670-a123-69bb28d891a5
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: NdrDllCanUnloadNow, NdrDllCanUnloadNow function [RPC], rpc.ndrdllcanunloadnow, rpcproxy/NdrDllCanUnloadNow
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcproxy.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: NDR_USER_MARSHAL_INFO_LEVEL1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RpcRT4.dll
api_name:
 - NdrDllCanUnloadNow
product: Windows
targetos: Windows
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
req.product: ADAM
---

# NdrDllCanUnloadNow function


## -description


The <b>NdrDllCanUnloadNow</b> function determines whether the DLL that implements the proxy and stub is still in use. If not, the caller can safely unload the DLL from memory.


## -parameters




### -param pPSFactoryBuffer [in]

Pointer to the <a href="_com_ipsfactorybuffer">CStdPSFactoryBuffer</a> object. The pointer is contained in the global variable, gPFactory, defined in RpcProxy.h. 


## -returns



Returns S_OK if the DLL can be unloaded. Otherwise, it returns S_FALSE if the DLL cannot be unloaded.



