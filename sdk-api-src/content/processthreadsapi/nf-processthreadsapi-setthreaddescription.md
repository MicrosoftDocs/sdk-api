---
UID: NF:processthreadsapi.SetThreadDescription
title: SetThreadDescription function (processthreadsapi.h)
description: Assigns a description to a thread.
helpviewer_keywords: ["SetThreadDescription","SetThreadDescription function","base.setthreaddescription","processthreadsapi/SetThreadDescription"]
old-location: base\setthreaddescription.htm
tech.root: processthreadsapi
ms.assetid: 0C17C60A-8DC9-4DB1-A3ED-5AFEBE598CBB
ms.date: 12/05/2018
ms.keywords: SetThreadDescription, SetThreadDescription function, base.setthreaddescription, processthreadsapi/SetThreadDescription
req.header: processthreadsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - SetThreadDescription
 - processthreadsapi/SetThreadDescription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-processthreads-l1-1-8.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
 - api-ms-win-core-processthreads-l1-1-6.dll
 - api-ms-win-core-processthreads-l1-1-5.dll
 - api-ms-win-core-processthreads-l1-1-4.dll
 - Kernel32.dll
 - KernelBase.dll
 - Api-ms-win-core-processthreads-l1-1-3.dll
api_name:
 - SetThreadDescription
---

# SetThreadDescription function


## -description

Assigns a description to a thread.

## -parameters

### -param hThread [in]

A handle for the thread for which you want to set the description. The handle must have THREAD_SET_LIMITED_INFORMATION access.

### -param lpThreadDescription [in]

A Unicode string that specifies the description of the thread.

## -returns

If the function succeeds, the return value is the **HRESULT** that denotes a successful operation.
If the function fails, the return value is an **HRESULT** that denotes the error.

## -remarks

The description of a thread can be set more than once; the most recently set value is used. You can retrieve the description of a thread by calling [GetThreadDescription](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreaddescription).

<b>Windows Server 2016</b>, <b>Windows 10 LTSB 2016</b> and <b>Windows 10 version 1607</b>: SetThreadDescription is only available by [Run Time Dynamic Linking](/windows/win32/dlls/using-run-time-dynamic-linking) in KernelBase.dll.

#### Examples

The following example sets the description for the current thread to `simulation_thread`.

```cpp
HRESULT hr = SetThreadDescription(GetCurrentThread(), L"simulation_thread");
if (FAILED(hr))
{
    // Call failed.
}
```

## -see-also

[GetThreadDescription](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreaddescription), [How to: Set a Thread Name in Native Code](/visualstudio/debugger/how-to-set-a-thread-name-in-native-code)
