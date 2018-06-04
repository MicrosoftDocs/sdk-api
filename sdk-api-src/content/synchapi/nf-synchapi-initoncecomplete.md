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

# InitOnceComplete function


## -description


Completes one-time initialization started with the <a href="https://msdn.microsoft.com/f342e85c-ac81-4470-89ce-a9d0fc5e8f89">InitOnceBeginInitialize</a> function.


## -parameters




### -param lpInitOnce [in, out]

A pointer to the one-time initialization structure.


### -param dwFlags [in]

This parameter can be one of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INIT_ONCE_ASYNC"></a><a id="init_once_async"></a><dl>
<dt><b>INIT_ONCE_ASYNC</b></dt>
<dt>0x00000002UL</dt>
</dl>
</td>
<td width="60%">
Operate in asynchronous mode. This enables multiple completion attempts to execute in parallel. This flag must match the flag passed in the corresponding call to the <a href="https://msdn.microsoft.com/f342e85c-ac81-4470-89ce-a9d0fc5e8f89">InitOnceBeginInitialize</a> function. This flag may not be combined with <b>INIT_ONCE_INIT_FAILED</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="INIT_ONCE_INIT_FAILED"></a><a id="init_once_init_failed"></a><dl>
<dt><b>INIT_ONCE_INIT_FAILED</b></dt>
<dt>0x00000004UL</dt>
</dl>
</td>
<td width="60%">
The initialization attempt failed. This flag may not be combined with <b>INIT_ONCE_ASYNC</b>. To fail an asynchronous initialization, merely abandon it (that is, do not call the <b>InitOnceComplete</b> function).

</td>
</tr>
</table>
 


### -param lpContext [in, optional]

A pointer to the data to be stored with the one-time initialization structure. This data is returned in the <i>lpContext</i> parameter passed to subsequent calls to the <a href="https://msdn.microsoft.com/f342e85c-ac81-4470-89ce-a9d0fc5e8f89">InitOnceBeginInitialize</a> function. If <i>lpContext</i> points to a value, the low-order <b>INIT_ONCE_CTX_RESERVED_BITS</b> of the value must be zero. If <i>lpContext</i>  points to a data structure, the data structure must be <b>DWORD</b>-aligned.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.


#### Examples

For an example that uses 
this function, see 
<a href="https://msdn.microsoft.com/47e68fbb-29f8-4930-beba-01d44263eb1e">Using One-Time Initialization</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/f342e85c-ac81-4470-89ce-a9d0fc5e8f89">InitOnceBeginInitialize</a>



<a href="https://msdn.microsoft.com/404c083c-7bee-44c2-b8e7-da1901b6ab2f">One-Time Initialization</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

