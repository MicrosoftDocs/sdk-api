---
UID: NF:rpcnsi.RpcNsMgmtEntryInqIfIdsA
title: RpcNsMgmtEntryInqIfIdsA function (rpcnsi.h)
description: The RpcNsMgmtEntryInqIfIds function returns the list of interfaces exported to a name service database entry. (ANSI)
helpviewer_keywords: ["RpcNsMgmtEntryInqIfIdsA", "rpcnsi/RpcNsMgmtEntryInqIfIdsA"]
old-location: rpc\rpcnsmgmtentryinqifids.htm
tech.root: Rpc
ms.assetid: 92f33e1d-a054-4484-903a-c91d3cd549d1
ms.date: 12/05/2018
ms.keywords: RpcNsMgmtEntryInqIfIds, RpcNsMgmtEntryInqIfIds function [RPC], RpcNsMgmtEntryInqIfIdsA, RpcNsMgmtEntryInqIfIdsW, _rpc_rpcnsmgmtentryinqifids, rpc.rpcnsmgmtentryinqifids, rpcnsi/RpcNsMgmtEntryInqIfIds, rpcnsi/RpcNsMgmtEntryInqIfIdsA, rpcnsi/RpcNsMgmtEntryInqIfIdsW
req.header: rpcnsi.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsMgmtEntryInqIfIdsW (Unicode) and RpcNsMgmtEntryInqIfIdsA (ANSI)
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
 - RpcNsMgmtEntryInqIfIdsA
 - rpcnsi/RpcNsMgmtEntryInqIfIdsA
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
 - RpcNsMgmtEntryInqIfIds
 - RpcNsMgmtEntryInqIfIdsA
 - RpcNsMgmtEntryInqIfIdsW
---

# RpcNsMgmtEntryInqIfIdsA function


## -description

The 
<b>RpcNsMgmtEntryInqIfIds</b> function returns the list of interfaces exported to a name service–database entry. It also returns an interface-identification vector containing the interfaces of binding handles exported by a server to <i>EntryName</i>. This function uses an expiration age of 0, causing an immediate update of the local copy of name-service data.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param EntryNameSyntax

Syntax of <i>EntryName</i>. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.

### -param EntryName

Pointer to the name service–database entry name for which an interface-identification vector is returned.

### -param IfIdVec

Returns an address of a pointer to the interface-identification vector.

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
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcNsMgmtEntryInqIfIds</b> function returns an interface-identification vector containing the interfaces of binding handles exported by a server to <i>EntryName</i>. This function uses an expiration age of 0, causing an immediate update of the local copy of name-service data. The calling application is responsible for calling the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcifidvectorfree">RpcIfIdVectorFree</a> function to release memory used by the vector.





> [!NOTE]
> The rpcnsi.h header defines RpcNsMgmtEntryInqIfIds as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcifidvectorfree">RpcIfIdVectorFree</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcifinqid">RpcIfInqId</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta">RpcNsBindingExport</a>
