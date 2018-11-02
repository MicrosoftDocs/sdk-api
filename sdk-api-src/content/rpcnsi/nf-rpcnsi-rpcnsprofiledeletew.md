---
UID: NF:rpcnsi.RpcNsProfileDeleteW
title: RpcNsProfileDeleteW function
author: windows-sdk-content
description: The RpcNsProfileDelete function deletes a profile attribute.
old-location: rpc\rpcnsprofiledelete.htm
tech.root: rpc
ms.assetid: bac77a37-a4e8-4edf-a31b-28692ccec0f7
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: RpcNsProfileDelete, RpcNsProfileDelete function [RPC], RpcNsProfileDeleteA, RpcNsProfileDeleteW, _rpc_rpcnsprofiledelete, rpc.rpcnsprofiledelete, rpcnsi/RpcNsProfileDelete, rpcnsi/RpcNsProfileDeleteA, rpcnsi/RpcNsProfileDeleteW
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
req.unicode-ansi: RpcNsProfileDeleteW (Unicode) and RpcNsProfileDeleteA (ANSI)
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
 - RpcNsProfileDelete
 - RpcNsProfileDeleteA
 - RpcNsProfileDeleteW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcNsProfileDeleteW function


## -description


The 
<b>RpcNsProfileDelete</b> function deletes a profile attribute.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters




### -param ProfileNameSyntax

Integer value indicating the syntax of the next parameter, <i>ProfileName</i>. 




To use the syntax specified in the registry value <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.


### -param ProfileName

Pointer to the name of the profile to delete.


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
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcNsProfileDelete</b> function deletes the profile attribute from the specified name-service entry (<i>ProfileName</i>). Neither <i>ProfileName</i> nor the entry names included as members in each profile element are deleted.

<div class="alert"><b>Note</b>  Use 
<b>RpcNsProfileDelete</b> cautiously; deleting a profile can have the unwanted effect of breaking a hierarchy of profiles.</div>
<div> </div>
<div class="alert"><b>Note</b>  This DCE function is not supported by Microsoft Locator. Windows NT and Windows 2000 support the use of this function with Cell Directory Service (CDS) only.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/e0a2d4b9-853c-4578-8a15-e0be7bfc0b9b">RpcNsProfileEltAdd</a>



<a href="https://msdn.microsoft.com/303df924-73ad-4e2f-aa30-e600bb5594c2">RpcNsProfileEltRemove</a>
 

 

