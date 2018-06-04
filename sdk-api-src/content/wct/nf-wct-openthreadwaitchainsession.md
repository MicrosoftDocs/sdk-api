---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# OpenThreadWaitChainSession function


## -description


Creates a new WCT session.


## -parameters




### -param Flags [in]

The session type. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
A synchronous session.

</td>
</tr>
<tr>
<td width="40%"><a id="WCT_ASYNC_OPEN_FLAG"></a><a id="wct_async_open_flag"></a><dl>
<dt><b>WCT_ASYNC_OPEN_FLAG</b></dt>
</dl>
</td>
<td width="60%">
An asynchronous session.

</td>
</tr>
</table>
 


### -param callback [in, optional]

If the session is asynchronous, this parameter can be a pointer to a <a href="https://msdn.microsoft.com/07d987b4-3ee4-4957-a6e8-542c427b94dd">WaitChainCallback</a> callback function.


## -returns



If the function succeeds, the return value is a handle to the newly created session.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



When you have finished using the session, call the <a href="https://msdn.microsoft.com/dc288418-01e4-4737-9c63-e6e6b73b5d13">CloseThreadWaitChainSession</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/7c5fa606-6e9b-41da-bfa9-1f066449d813">Using WCT</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/dc288418-01e4-4737-9c63-e6e6b73b5d13">CloseThreadWaitChainSession</a>



<a href="https://msdn.microsoft.com/5b418fa6-1d07-465e-85ea-b7127264eebf">GetThreadWaitChain</a>



<a href="https://msdn.microsoft.com/d266a663-b101-4936-9574-f6ce223419ae">Wait Chain Traversal</a>



<a href="https://msdn.microsoft.com/07d987b4-3ee4-4957-a6e8-542c427b94dd">WaitChainCallback</a>
 

 

