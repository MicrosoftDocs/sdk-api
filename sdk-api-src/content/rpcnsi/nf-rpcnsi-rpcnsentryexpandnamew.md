---
UID: NF:rpcnsi.RpcNsEntryExpandNameW
title: RpcNsEntryExpandNameW function (rpcnsi.h)
description: The RpcNsEntryExpandName function expands a name-service entry name. This function is supported by Active Directory.helpviewer_keywords: ["RpcNsEntryExpandName","RpcNsEntryExpandName function [RPC]","RpcNsEntryExpandNameA","RpcNsEntryExpandNameW","_rpc_rpcnsentryexpandname","rpc.rpcnsentryexpandname","rpcnsi/RpcNsEntryExpandName","rpcnsi/RpcNsEntryExpandNameA","rpcnsi/RpcNsEntryExpandNameW"]
old-location: rpc\rpcnsentryexpandname.htm
tech.root: Rpc
ms.assetid: a93052c2-3fb1-448a-b4bf-70b9676de69a
ms.date: 12/05/2018
ms.keywords: RpcNsEntryExpandName, RpcNsEntryExpandName function [RPC], RpcNsEntryExpandNameA, RpcNsEntryExpandNameW, _rpc_rpcnsentryexpandname, rpc.rpcnsentryexpandname, rpcnsi/RpcNsEntryExpandName, rpcnsi/RpcNsEntryExpandNameA, rpcnsi/RpcNsEntryExpandNameW
f1_keywords:
- rpcnsi/RpcNsEntryExpandName
dev_langs:
- c++
req.header: rpcnsi.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsEntryExpandNameW (Unicode) and RpcNsEntryExpandNameA (ANSI)
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
- RpcNsEntryExpandName
- RpcNsEntryExpandNameA
- RpcNsEntryExpandNameW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RpcNsEntryExpandNameW function


## -description


The 
<b>RpcNsEntryExpandName</b> function expands a name-service entry name. This function is supported by Active Directory.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters




### -param EntryNameSyntax

Syntax of <i>EntryName</i>. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of <b>RPC_C_NS_SYNTAX_DEFAULT</b>.


### -param EntryName

Pointer to the entry name to expand.


### -param ExpandedName

Returns a pointer to a pointer to the expanded version of <i>EntryName</i>.


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
<dt><b>RPC_S_INCOMPLETE_NAME</b></dt>
</dl>
</td>
<td width="60%">
The name is incomplete.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://docs.microsoft.com/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>



## -remarks



An application calls the 
<b>RpcNsEntryExpandName</b> function to obtain a fully expanded entry name.

The RPC run-time library allocates memory for the returned <i>ExpandedName</i> parameter. The application is responsible for calling the 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a> function for that returned string.

The returned expanded entry name accounts for local name translations and for differences in locally defined naming schema.

<div class="alert"><b>Note</b>  This function requires Active Directory support.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a>
 

 

