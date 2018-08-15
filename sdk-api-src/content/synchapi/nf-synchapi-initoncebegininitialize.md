---
UID: NF:synchapi.InitOnceBeginInitialize
title: InitOnceBeginInitialize function
author: windows-sdk-content
description: Begins one-time initialization.
old-location: base\initoncebegininitialize.htm
old-project: sync
ms.assetid: f342e85c-ac81-4470-89ce-a9d0fc5e8f89
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: INIT_ONCE_ASYNC, INIT_ONCE_CHECK_ONLY, InitOnceBeginInitialize, InitOnceBeginInitialize function, base.initoncebegininitialize, synchapi/InitOnceBeginInitialize, winbase/InitOnceBeginInitialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: synchapi.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.redist: 
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
tech.root: 
req.typenames: ITEMPROP, *LPITEMPROP
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
 - InitOnceBeginInitialize
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# InitOnceBeginInitialize function


## -description


Begins one-time initialization.


## -parameters




### -param lpInitOnce [in, out]

A pointer to the one-time initialization structure.


### -param dwFlags [in]

This parameter can be one or more of the following flags.

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
Enables multiple initialization attempts to execute in parallel. If this flag is used, subsequent calls to this function will fail unless this flag is also specified.

</td>
</tr>
<tr>
<td width="40%"><a id="INIT_ONCE_CHECK_ONLY"></a><a id="init_once_check_only"></a><dl>
<dt><b>INIT_ONCE_CHECK_ONLY</b></dt>
<dt>0x00000001UL</dt>
</dl>
</td>
<td width="60%">
This function call does not begin initialization. The return value indicates whether initialization has already completed. If the function returns <b>TRUE</b>, the <i>lpContext</i> parameter receives the data.

</td>
</tr>
</table>
 


### -param fPending [out]

If the function succeeds, this parameter indicates the current initialization status. 

If this parameter is <b>TRUE</b> and <i>dwFlags</i> contains <b>INIT_ONCE_CHECK_ONLY</b>, the initialization is pending and the context data is invalid.

If this parameter is <b>FALSE</b>, initialization has already completed and the caller can retrieve the context data from the <i>lpContext</i> parameter.

If this parameter is <b>TRUE</b> and <i>dwFlags</i> does not contain <b>INIT_ONCE_CHECK_ONLY</b>, initialization has been started and the caller can perform the initialization tasks.


### -param lpContext [out, optional]

An optional parameter that receives the data stored with the one-time initialization structure upon success. The low-order <b>INIT_ONCE_CTX_RESERVED_BITS</b> bits of the data are always zero.


## -returns



If <b>INIT_ONCE_CHECK_ONLY</b> is not specified and the function succeeds, the return value is <b>TRUE</b>.

If <b>INIT_ONCE_CHECK_ONLY</b> is specified and initialization has completed, the return value is <b>TRUE</b>.

Otherwise, the return value is <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function can be used for either synchronous or asynchronous one-time initialization. For asynchronous one-time initialization, use the <b>INIT_ONCE_ASYNC</b> flag. To specify a callback function to execute during synchronous one-time initialization, see the <a href="https://msdn.microsoft.com/04c161ed-d1b0-4995-b246-cb64cb67ae47">InitOnceExecuteOnce</a> function.

If this function succeeds, the thread can create a synchronization object and specify in the <i>lpContext</i> parameter of the <a href="https://msdn.microsoft.com/aad1d1f6-5415-443a-94d2-f4a4d9b68750">InitOnceComplete</a> function.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.

A one-time initialization object cannot be moved or copied. The process must not modify the initialization object, and must instead treat it as logically opaque. Only use the one-time initialization functions to manage one-time initialization objects.


#### Examples

For an example that uses 
this function, see 
<a href="https://msdn.microsoft.com/47e68fbb-29f8-4930-beba-01d44263eb1e">Using One-Time Initialization</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/aad1d1f6-5415-443a-94d2-f4a4d9b68750">InitOnceComplete</a>



<a href="https://msdn.microsoft.com/04c161ed-d1b0-4995-b246-cb64cb67ae47">InitOnceExecuteOnce</a>



<a href="https://msdn.microsoft.com/404c083c-7bee-44c2-b8e7-da1901b6ab2f">One-Time Initialization</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

