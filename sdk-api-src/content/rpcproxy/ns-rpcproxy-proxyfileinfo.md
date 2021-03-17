---
UID: NS:rpcproxy.tagProxyFileInfo
title: ProxyFileInfo (rpcproxy.h)
description: The ProxyFileInfo structure contains information about the interface proxies in the proxy DLL.
helpviewer_keywords: ["ExtendedProxyFileInfo","ProxyFileInfo","ProxyFileInfo structure [RPC]","rpc.proxyfileinfo","rpcproxy/ProxyFileInfo"]
old-location: rpc\proxyfileinfo.htm
tech.root: Rpc
ms.assetid: dbe797da-3ec3-4fe0-83bf-30669127a401
ms.date: 12/05/2018
ms.keywords: ExtendedProxyFileInfo, ProxyFileInfo, ProxyFileInfo structure [RPC], rpc.proxyfileinfo, rpcproxy/ProxyFileInfo
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ProxyFileInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagProxyFileInfo
 - rpcproxy/tagProxyFileInfo
 - ProxyFileInfo
 - rpcproxy/ProxyFileInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcproxy.h
api_name:
 - ProxyFileInfo
---

# ProxyFileInfo structure


## -description

The <b>ProxyFileInfo</b> structure contains information about the interface proxies in the proxy DLL.

## -struct-fields

### -field pProxyVtblList

Array of proxy Vtables contained in the proxy DLL. Each array element contains the Vtable for each proxy interface in the DLL.

### -field pStubVtblList

### -field pNamesArray

Array of interface names contained in the proxy DLL.

### -field pDelegatedIIDs

Array of base interface identifiers contained in the proxy DLL. Array elements associated with interfaces that are not delegated are set to null. If no interfaces in the DLL are delegated, <i>pDelegatedIIDs</i> is null.

### -field pIIDLookupRtn

Used to search for a given interface in the proxy list.

### -field TableSize

Number of interfaces in the proxy DLL.

### -field TableVersion

Version of the proxy stub. The version can be one of the versions.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The .idl file is compiled with the <a href="/windows/desktop/Midl/-os">/0s</a> option. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The .idl file is compiled with the <a href="/windows/desktop/Midl/-oi">/0i</a>, <b>/0ic</b>, or <b>/Oicf</b> option.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The proxy DLL contains an asynchronous interface.

</td>
</tr>
</table>

### -field pAsyncIIDLookup

Used to search for a given asynchronous interface in the proxy list.

### -field Filler2

Not used.

### -field Filler3

Not used.

### -field Filler4

Not used.

### -field pstubVtblList

Array of stub Vtables contained in the proxy DLL. Each array element contains the Vtable for each stub interface in the DLL.