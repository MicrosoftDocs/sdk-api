---
UID: NF:rpcdce.UuidEqual
title: UuidEqual function
author: windows-sdk-content
description: An application calls the UuidEqual function to compare two UUIDs and determine whether they are equal.
old-location: rpc\uuidequal.htm
old-project: rpc
ms.assetid: ff83c66c-1f1f-4582-a93b-d7bb5181deec
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: UuidEqual, UuidEqual function [RPC], _rpc_uuidequal, rpc.uuidequal, rpcdce/UuidEqual
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - UuidEqual
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: ADAM
---

# UuidEqual function


## -description


An application calls the  
<b>UuidEqual</b> function to compare two <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a>s and determine whether they are equal.


## -parameters




### -param Uuid1

Pointer to a 
<a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a>. This <b>UUID</b> is compared with the <b>UUID</b> specified in the <i>Uuid2</i> parameter.


### -param Uuid2

Pointer to a <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a>. This <b>UUID</b> is compared with the <b>UUID</b> specified in the <i>Uuid1</i> parameter.


### -param Status

Returns RPC_S_OK.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The <i>Uuid1</i> parameter is equal to the <i>Uuid2</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The <i>Uuid1</i> parameter is not equal to the <i>Uuid2</i> parameter.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/4008fb54-7770-4f1a-8e1c-4b20bef884f9">UuidCreate</a>
 

 

