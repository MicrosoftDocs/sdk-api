---
UID: NF:synchapi.InitOnceComplete
title: InitOnceComplete function
author: windows-sdk-content
description: Completes one-time initialization started with the InitOnceBeginInitialize function.
old-location: base\initoncecomplete.htm
tech.root: sync
ms.assetid: aad1d1f6-5415-443a-94d2-f4a4d9b68750
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: INIT_ONCE_ASYNC, INIT_ONCE_INIT_FAILED, InitOnceComplete, InitOnceComplete function, base.initoncecomplete, synchapi/InitOnceComplete, winbase/InitOnceComplete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: synchapi.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Synch-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Synch-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - InitOnceComplete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- InitOnceComplete
: 
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
 

 

