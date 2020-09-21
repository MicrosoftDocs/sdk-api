---
UID: NF:rpcdce.UuidCreate
title: UuidCreate function (rpcdce.h)
description: The UuidCreate function creates a new UUID.
helpviewer_keywords: ["UuidCreate","UuidCreate function [RPC]","_rpc_uuidcreate","rpc.uuidcreate","rpcdce/UuidCreate"]
old-location: rpc\uuidcreate.htm
tech.root: Rpc
ms.assetid: 4008fb54-7770-4f1a-8e1c-4b20bef884f9
ms.date: 12/05/2018
ms.keywords: UuidCreate, UuidCreate function [RPC], _rpc_uuidcreate, rpc.uuidcreate, rpcdce/UuidCreate
req.header: rpcdce.h
req.include-header: Rpc.h
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
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UuidCreate
 - rpcdce/UuidCreate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - UuidCreate
---

# UuidCreate function


## -description

The 
<b>UuidCreate</b> function creates a new 
<a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a>.

## -parameters

### -param Uuid

Returns a pointer to the created <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a>.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_UUID_LOCAL_ONLY</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a> is guaranteed to be unique to this computer only.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_UUID_NO_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
Cannot get Ethernet or token-ring hardware address for this computer.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

For security reasons, it is often desirable to keep ethernet addresses on networks from becoming available outside a company or organization. The 
<b>UuidCreate</b> function generates a <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a> that cannot be traced to the ethernet address of the computer on which it was generated. It also cannot be associated with other <b>UUID</b>s created on the same computer. If you do not need this level of security, your application can use the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreatesequential">UuidCreateSequential</a> function, which behaves exactly as the 
<b>UuidCreate</b> function does on all other versions of the operating system.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidfromstring">UuidFromString</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring">UuidToString</a>