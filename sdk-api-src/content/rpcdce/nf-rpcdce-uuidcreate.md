---
UID: NF:rpcdce.UuidCreate
title: UuidCreate function
author: windows-driver-content
description: The UuidCreate function creates a new UUID.
old-location: rpc\uuidcreate.htm
old-project: Rpc
ms.assetid: 4008fb54-7770-4f1a-8e1c-4b20bef884f9
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: UuidCreate, UuidCreate function [RPC], _rpc_uuidcreate, rpc.uuidcreate, rpcdce/UuidCreate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rpcrt4.dll
api_name:
-	UuidCreate
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# UuidCreate function


## -description



			The 
<b>UuidCreate</b> function creates a new 
<a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a>.


## -parameters




### -param Uuid

Returns a pointer to the created <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a>.


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
The <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a> is guaranteed to be unique to this computer only.

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
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



For security reasons, it is often desirable to keep ethernet addresses on networks from becoming available outside a company or organization. The 
<b>UuidCreate</b> function generates a <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a> that cannot be traced to the ethernet address of the computer on which it was generated. It also cannot be associated with other <b>UUID</b>s created on the same computer. If you do not need this level of security, your application can use the 
<a href="https://msdn.microsoft.com/66975d82-559c-4a13-846c-e403b015563b">UuidCreateSequential</a> function, which behaves exactly as the 
<b>UuidCreate</b> function does on all other versions of the operating system.




## -see-also




<a href="https://msdn.microsoft.com/90b3cf6b-a15b-4f91-9ba2-0e43fe3374df">UuidFromString</a>



<a href="https://msdn.microsoft.com/49235b28-a0c5-4f69-9932-85350d7bcbb8">UuidToString</a>
 

 

