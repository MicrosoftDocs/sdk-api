---
UID: NF:rpcnsi.RpcNsGroupMbrRemoveA
title: RpcNsGroupMbrRemoveA function (rpcnsi.h)
description: The RpcNsGroupMbrRemove function removes an entry name from a group. (ANSI)
helpviewer_keywords: ["RpcNsGroupMbrRemoveA", "rpcnsi/RpcNsGroupMbrRemoveA"]
old-location: rpc\rpcnsgroupmbrremove.htm
tech.root: Rpc
ms.assetid: 0301b570-9a03-4f50-89df-3c15d8de246f
ms.date: 12/05/2018
ms.keywords: RpcNsGroupMbrRemove, RpcNsGroupMbrRemove function [RPC], RpcNsGroupMbrRemoveA, RpcNsGroupMbrRemoveW, _rpc_rpcnsgroupmbrremove, rpc.rpcnsgroupmbrremove, rpcnsi/RpcNsGroupMbrRemove, rpcnsi/RpcNsGroupMbrRemoveA, rpcnsi/RpcNsGroupMbrRemoveW
req.header: rpcnsi.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsGroupMbrRemoveW (Unicode) and RpcNsGroupMbrRemoveA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcns4.lib
req.dll: Rpcns4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcNsGroupMbrRemoveA
 - rpcnsi/RpcNsGroupMbrRemoveA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcns4.dll
api_name:
 - RpcNsGroupMbrRemove
 - RpcNsGroupMbrRemoveA
 - RpcNsGroupMbrRemoveW
---

# RpcNsGroupMbrRemoveA function


## -description

The 
<b>RpcNsGroupMbrRemove</b> function removes an entry name from a group.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param GroupNameSyntax

Syntax of <i>GroupName</i>. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.

### -param GroupName

Pointer to the name of the RPC group from which to remove the member name.

### -param MemberNameSyntax

Syntax to use in the <i>MemberName</i> parameter. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.

### -param MemberName

Pointer to the name of the member to remove from the RPC group attribute in the entry <i>GroupName</i>.

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
<dt><b>RPC_S_INVALID_NAME_SYNTAX</b></dt>
</dl>
</td>
<td width="60%">
The name syntax is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_UNSUPPORTED_NAME_SYNTAX</b></dt>
</dl>
</td>
<td width="60%">
The name syntax is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INCOMPLETE_NAME</b></dt>
</dl>
</td>
<td width="60%">
The name is incomplete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_ENTRY_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The name-service entry was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NAME_SERVICE_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The name service is unavailable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_GROUP_MEMBER_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The group member was not found.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcNsGroupMbrRemove</b> function removes a member from the RPC group attribute in the <i>GroupName</i> parameter.

<div class="alert"><b>Note</b>  Windows 2000 Active Directory supports this function. Earlier versions of Windows NT support the use of this function with Cell Directory Service (CDS) only.</div>
<div> </div>




> [!NOTE]
> The rpcnsi.h header defines RpcNsGroupMbrRemove as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsgroupmbradda">RpcNsGroupMbrAdd</a>
