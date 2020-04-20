---
UID: NF:rpcproxy.NdrDllGetClassObject
title: NdrDllGetClassObject function (rpcproxy.h)
description: The NdrDllGetClassObject function retrieves the class object of the proxy or stub.helpviewer_keywords: ["NdrDllGetClassObject","NdrDllGetClassObject function [RPC]","rpc.ndrdllgetclassobject","rpcproxy/NdrDllGetClassObject"]
old-location: rpc\ndrdllgetclassobject.htm
tech.root: Rpc
ms.assetid: 322e0a8c-1eda-4148-a7cc-7f7fd7bf0b6f
ms.date: 12/05/2018
ms.keywords: NdrDllGetClassObject, NdrDllGetClassObject function [RPC], rpc.ndrdllgetclassobject, rpcproxy/NdrDllGetClassObject
f1_keywords:
- rpcproxy/NdrDllGetClassObject
dev_langs:
- c++
req.header: rpcproxy.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
- NdrDllGetClassObject
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NdrDllGetClassObject function


## -description


The <b>NdrDllGetClassObject</b> function retrieves the class object of the proxy or stub.


## -parameters




### -param rclsid [in]

Class identifier of the proxy or stub to retrieve.


### -param riid [in]

Interface identifier of the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipsfactorybuffer">IPSFactoryBuffer</a> interface.


### -param ppv [out]

Address of the output variable that receives the interface pointer requested in <i>riid</i>.


### -param pProxyFileList [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/rpcproxy/ns-rpcproxy-proxyfileinfo">ProxyFileInfo</a> structure, which contains information about the proxy and stub.


### -param pclsid [in]

Pointer to the class identifier of the proxy or stub. Specify <i>pclsid</i> if the <b>PROXY_CLSID</b> constant is defined in the source code or as a C compiler option.


### -param pPSFactoryBuffer [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipsfactorybuffer">IPSFactoryBuffer</a> object.  The pointer is contained in the global variable, gPFactory, defined in RpcProxy.h.


## -returns



Returns S_OK on success.



