---
UID: NF:rpcnsi.RpcNsMgmtEntryDeleteW
title: RpcNsMgmtEntryDeleteW function
author: windows-sdk-content
description: The RpcNsMgmtEntryDelete function deletes a name service&#8211;database entry.
old-location: rpc\rpcnsmgmtentrydelete.htm
tech.root: rpc
ms.assetid: 65d04a7c-e42c-4956-a953-b9aec95254e0
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: RpcNsMgmtEntryDelete, RpcNsMgmtEntryDelete function [RPC], RpcNsMgmtEntryDeleteA, RpcNsMgmtEntryDeleteW, _rpc_rpcnsmgmtentrydelete, rpc.rpcnsmgmtentrydelete, rpcnsi/RpcNsMgmtEntryDelete, rpcnsi/RpcNsMgmtEntryDeleteA, rpcnsi/RpcNsMgmtEntryDeleteW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcnsi.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsMgmtEntryDeleteW (Unicode) and RpcNsMgmtEntryDeleteA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcns4.lib
req.dll: Rpcns4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcns4.dll
api_name:
 - RpcNsMgmtEntryDelete
 - RpcNsMgmtEntryDeleteA
 - RpcNsMgmtEntryDeleteW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcNsMgmtEntryDeleteW function


## -description


The 
<b>RpcNsMgmtEntryDelete</b> function deletes a name service–database entry.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters




### -param EntryNameSyntax

Syntax of <i>EntryName</i>. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.


### -param EntryName

Pointer to the name of the entry to delete.


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
<dt><b>RPC_S_NOT_RPC_ENTRY</b></dt>
</dl>
</td>
<td width="60%">
Not an RPC entry.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



Management applications use the 
<b>RpcNsMgmtEntryDelete</b> function only when an entry is no longer needed—for example, when a server is being permanently removed from service.

Because name-service databases are designed to be relatively stable, frequent use of 
<b>RpcNsMgmtEntryDelete</b> in client or server applications can result in performance problems. Creating and deleting entries in client or server applications causes the name-service database to repeatedly remove and replace the same entry. This can lead to performance problems in replicated name-service databases.




## -see-also




<a href="https://msdn.microsoft.com/32de2395-174a-4e14-82db-9043db817708">RpcNsMgmtEntryCreate</a>
 

 

