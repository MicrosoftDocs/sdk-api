---
UID: NF:rpcnsi.RpcNsGroupMbrAddA
title: RpcNsGroupMbrAddA function (rpcnsi.h)
description: The RpcNsGroupMbrAdd function adds an entry name to a group. If necessary, it creates the entry. (ANSI)
helpviewer_keywords: ["RpcNsGroupMbrAddA", "rpcnsi/RpcNsGroupMbrAddA"]
old-location: rpc\rpcnsgroupmbradd.htm
tech.root: Rpc
ms.assetid: fa32b5e5-1a8a-44f4-aa38-81b024f4db51
ms.date: 12/05/2018
ms.keywords: RpcNsGroupMbrAdd, RpcNsGroupMbrAdd function [RPC], RpcNsGroupMbrAddA, RpcNsGroupMbrAddW, _rpc_rpcnsgroupmbradd, rpc.rpcnsgroupmbradd, rpcnsi/RpcNsGroupMbrAdd, rpcnsi/RpcNsGroupMbrAddA, rpcnsi/RpcNsGroupMbrAddW
req.header: rpcnsi.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsGroupMbrAddW (Unicode) and RpcNsGroupMbrAddA (ANSI)
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
 - RpcNsGroupMbrAddA
 - rpcnsi/RpcNsGroupMbrAddA
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
 - RpcNsGroupMbrAdd
 - RpcNsGroupMbrAddA
 - RpcNsGroupMbrAddW
---

# RpcNsGroupMbrAddA function


## -description

The 
<b>RpcNsGroupMbrAdd</b> function adds an entry name to a group. If necessary, it creates the entry.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param GroupNameSyntax

Syntax of <i>GroupName</i>. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.

### -param GroupName

Pointer to the name of the RPC group to receive a new member.

### -param MemberNameSyntax

Syntax to use in <i>MemberName</i>. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.

### -param MemberName

Pointer to the name of the new RPC group member.

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
<dt><b>RPC_S_NAME_SERVICE_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The name service is unavailable.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcNsGroupMbrAdd</b> adds a name service–database entry name as a member to the RPC group attribute.

If the <i>GroupName</i> entry does not exist, 
<b>RpcNsGroupMbrAdd</b> tries to create the entry with a group attribute and adds the group member specified by <i>MemberName</i>. In this case, the application must have the privilege to create the entry. Otherwise, a management application with the necessary privilege should create the entry by calling 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsmgmtentrycreatea">RpcNsMgmtEntryCreate</a> before the application is run.

<div class="alert"><b>Note</b>  Windows 2000 Active Directory supports this function. Earlier versions of Windows NT support the use of this function with Cell Directory Service (CDS) only.</div>
<div> </div>




> [!NOTE]
> The rpcnsi.h header defines RpcNsGroupMbrAdd as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsgroupmbrremovea">RpcNsGroupMbrRemove</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsmgmtentrycreatea">RpcNsMgmtEntryCreate</a>
