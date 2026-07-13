---
UID: NF:rpcnsi.RpcNsGroupDeleteW
title: RpcNsGroupDeleteW function (rpcnsi.h)
description: The RpcNsGroupDelete function deletes a group attribute. (Unicode)
helpviewer_keywords: ["RPC_C_NS_SYNTAX_DCE", "RPC_C_NS_SYNTAX_DEFAULT", "RpcNsGroupDelete", "RpcNsGroupDelete function [RPC]", "RpcNsGroupDeleteW", "_rpc_rpcnsgroupdelete", "rpc.rpcnsgroupdelete", "rpcnsi/RpcNsGroupDelete", "rpcnsi/RpcNsGroupDeleteW"]
old-location: rpc\rpcnsgroupdelete.htm
tech.root: Rpc
ms.assetid: 4455e891-7846-47b5-9283-549c3451b70e
ms.date: 12/05/2018
ms.keywords: RPC_C_NS_SYNTAX_DCE, RPC_C_NS_SYNTAX_DEFAULT, RpcNsGroupDelete, RpcNsGroupDelete function [RPC], RpcNsGroupDeleteA, RpcNsGroupDeleteW, _rpc_rpcnsgroupdelete, rpc.rpcnsgroupdelete, rpcnsi/RpcNsGroupDelete, rpcnsi/RpcNsGroupDeleteA, rpcnsi/RpcNsGroupDeleteW
req.header: rpcnsi.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsGroupDeleteW (Unicode) and RpcNsGroupDeleteA (ANSI)
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
 - RpcNsGroupDeleteW
 - rpcnsi/RpcNsGroupDeleteW
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
 - RpcNsGroupDelete
 - RpcNsGroupDeleteA
 - RpcNsGroupDeleteW
---

# RpcNsGroupDeleteW function


## -description

The 
<b>RpcNsGroupDelete</b> function deletes a group attribute.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param GroupNameSyntax

Integer value that indicates the syntax of <i>GroupName</i>. Can be set to one of the following values: 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RPC_C_NS_SYNTAX_DEFAULT"></a><a id="rpc_c_ns_syntax_default"></a><dl>
<dt><b>RPC_C_NS_SYNTAX_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Use the syntax specified in the registry value <b>HKEY_LOCAL_MACHINE\
Software\Microsoft\Rpc\
NameService\
DefaultSyntax
							</b>

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_NS_SYNTAX_DCE"></a><a id="rpc_c_ns_syntax_dce"></a><dl>
<dt><b>RPC_C_NS_SYNTAX_DCE</b></dt>
</dl>
</td>
<td width="60%">
Use DCE syntax.

</td>
</tr>
</table>

### -param GroupName

Pointer to the name of the name-service group to delete.

## -returns

This function returns one of the following values:

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
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcNsGroupDelete</b> function deletes the group attribute from the specified name service–database entry.

Neither the specified name service–database entry nor the group members are deleted.

<div class="alert"><b>Note</b>  This DCE function is not supported by Microsoft Locator. Windows NT and Windows 2000 both support the use of this function, but with Cell Directory Service (CDS) only.</div>
<div> </div>




> [!NOTE]
> The rpcnsi.h header defines RpcNsGroupDelete as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsgroupmbradda">RpcNsGroupMbrAdd</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsgroupmbrremovea">RpcNsGroupMbrRemove</a>
