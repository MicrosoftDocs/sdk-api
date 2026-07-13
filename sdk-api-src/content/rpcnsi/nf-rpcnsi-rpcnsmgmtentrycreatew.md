---
UID: NF:rpcnsi.RpcNsMgmtEntryCreateW
title: RpcNsMgmtEntryCreateW function (rpcnsi.h)
description: The RpcNsMgmtEntryCreate function creates a name service database entry. (Unicode)
helpviewer_keywords: ["RpcNsMgmtEntryCreate", "RpcNsMgmtEntryCreate function [RPC]", "RpcNsMgmtEntryCreateW", "_rpc_rpcnsmgmtentrycreate", "rpc.rpcnsmgmtentrycreate", "rpcnsi/RpcNsMgmtEntryCreate", "rpcnsi/RpcNsMgmtEntryCreateW"]
old-location: rpc\rpcnsmgmtentrycreate.htm
tech.root: Rpc
ms.assetid: 32de2395-174a-4e14-82db-9043db817708
ms.date: 12/05/2018
ms.keywords: RpcNsMgmtEntryCreate, RpcNsMgmtEntryCreate function [RPC], RpcNsMgmtEntryCreateA, RpcNsMgmtEntryCreateW, _rpc_rpcnsmgmtentrycreate, rpc.rpcnsmgmtentrycreate, rpcnsi/RpcNsMgmtEntryCreate, rpcnsi/RpcNsMgmtEntryCreateA, rpcnsi/RpcNsMgmtEntryCreateW
req.header: rpcnsi.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsMgmtEntryCreateW (Unicode) and RpcNsMgmtEntryCreateA (ANSI)
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
 - RpcNsMgmtEntryCreateW
 - rpcnsi/RpcNsMgmtEntryCreateW
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
 - RpcNsMgmtEntryCreate
 - RpcNsMgmtEntryCreateA
 - RpcNsMgmtEntryCreateW
---

# RpcNsMgmtEntryCreateW function


## -description

The 
<b>RpcNsMgmtEntryCreate</b> function creates a name service–database entry.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param EntryNameSyntax

Syntax of <i>EntryName</i>. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.

### -param EntryName

Pointer to the name of the entry to create.

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
<dt><b>RPC_S_ENTRY_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The name-service entry already exists.

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
<b>RpcNsMgmtEntryCreate</b> function creates an entry in the name-service database. A management application can call 
<b>RpcNsMgmtEntryCreate</b> to create a name service–database entry for use by another application that does not itself have the necessary name service–database privileges to create an entry.

<div class="alert"><b>Note</b>  Windows 2000 Active Directory supports this function. Earlier versions of Windows NT support the use of this function with Cell Directory Service (CDS) only.</div>
<div> </div>




> [!NOTE]
> The rpcnsi.h header defines RpcNsMgmtEntryCreate as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsmgmtentrydeletea">RpcNsMgmtEntryDelete</a>
