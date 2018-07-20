---
UID: NF:rpcdce.UuidIsNil
title: UuidIsNil function
author: windows-sdk-content
description: An application calls the UuidIsNil function to determine whether the specified UUID is a nil-valued UUID.
old-location: rpc\uuidisnil.htm
old-project: rpc
ms.assetid: 0b764eca-552b-4431-812b-93fa0c03179e
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: UuidIsNil, UuidIsNil function [RPC], _rpc_uuidisnil, rpc.uuidisnil, rpcdce/UuidIsNil
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
 - UuidIsNil
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: ADAM
---

# UuidIsNil function


## -description



			An application calls the  
<b>UuidIsNil</b> function to determine whether the specified <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a> is a nil-valued <b>UUID</b>.


## -parameters




### -param Uuid


<a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a> to test for nil value.


### -param Status

Returns RPC_S_OK.


## -returns



<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



This function acts as though the application called 
<a href="https://msdn.microsoft.com/ee955482-e786-4478-bbaa-7c574ab1ecc5">UuidCreateNil</a>, and then called the 
<a href="https://msdn.microsoft.com/ff83c66c-1f1f-4582-a93b-d7bb5181deec">UuidEqual</a> to compare the returned nil-value <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a> to the <b>UUID</b> specified in the <i>Uuid</i> parameter.

Upon completion, one of the following values is returned.

<table>
<tr>
<th>Returned value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>The <i>Uuid</i> parameter is a nil-valued <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a>.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>The <i>Uuid</i> parameter is not a nil-valued <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a>.</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/4008fb54-7770-4f1a-8e1c-4b20bef884f9">UuidCreate</a>
 

 

