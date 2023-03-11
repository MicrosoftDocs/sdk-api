---
UID: NF:synchapi.InitOnceComplete
title: InitOnceComplete function (synchapi.h)
description: Completes one-time initialization started with the InitOnceBeginInitialize function.
helpviewer_keywords: ["INIT_ONCE_ASYNC","INIT_ONCE_INIT_FAILED","InitOnceComplete","InitOnceComplete function","base.initoncecomplete","synchapi/InitOnceComplete","winbase/InitOnceComplete"]
old-location: base\initoncecomplete.htm
tech.root: base
ms.assetid: aad1d1f6-5415-443a-94d2-f4a4d9b68750
ms.date: 12/05/2018
ms.keywords: INIT_ONCE_ASYNC, INIT_ONCE_INIT_FAILED, InitOnceComplete, InitOnceComplete function, base.initoncecomplete, synchapi/InitOnceComplete, winbase/InitOnceComplete
req.header: synchapi.h
req.include-header: Windows.h on Windows 7, Windows Server 2008  Windows Server 2008 R2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InitOnceComplete
 - synchapi/InitOnceComplete
dev_langs:
 - c++
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
---

# InitOnceComplete function


## -description

Completes one-time initialization started with the <a href="/windows/desktop/api/synchapi/nf-synchapi-initoncebegininitialize">InitOnceBeginInitialize</a> function.

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
Operate in asynchronous mode. This enables multiple completion attempts to execute in parallel. This flag must match the flag passed in the corresponding call to the <a href="/windows/desktop/api/synchapi/nf-synchapi-initoncebegininitialize">InitOnceBeginInitialize</a> function. This flag may not be combined with <b>INIT_ONCE_INIT_FAILED</b>.

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

A pointer to the data to be stored with the one-time initialization structure. This data is returned in the <i>lpContext</i> parameter passed to subsequent calls to the <a href="/windows/desktop/api/synchapi/nf-synchapi-initoncebegininitialize">InitOnceBeginInitialize</a> function. If <i>lpContext</i> points to a value, the low-order <b>INIT_ONCE_CTX_RESERVED_BITS</b> of the value must be zero. If <i>lpContext</i>  points to a data structure, the data structure must be <b>DWORD</b>-aligned.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.


#### Examples

For an example that uses 
this function, see 
<a href="/windows/desktop/Sync/using-one-time-initialization">Using One-Time Initialization</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/synchapi/nf-synchapi-initoncebegininitialize">InitOnceBeginInitialize</a>



<a href="/windows/desktop/Sync/one-time-initialization">One-Time Initialization</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>