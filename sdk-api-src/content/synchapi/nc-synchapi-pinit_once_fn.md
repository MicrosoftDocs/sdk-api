---
UID: NC:synchapi.PINIT_ONCE_FN
title: PINIT_ONCE_FN (synchapi.h)
description: An application-defined callback function. Specify a pointer to this function when calling the InitOnceExecuteOnce function.
helpviewer_keywords: ["PINIT_ONCE_FN","PINIT_ONCE_FN callback","PINIT_ONCE_FN callback function","base.initoncecallback","synchapi/PINIT_ONCE_FN"]
old-location: base\initoncecallback.htm
tech.root: base
ms.assetid: e4a73572-e477-4518-87fe-b9b74234e8ec
ms.date: 12/05/2018
ms.keywords: PINIT_ONCE_FN, PINIT_ONCE_FN callback, PINIT_ONCE_FN callback function, base.initoncecallback, synchapi/PINIT_ONCE_FN
req.header: synchapi.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PINIT_ONCE_FN
 - synchapi/PINIT_ONCE_FN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - synchapi.h
api_name:
 - PINIT_ONCE_FN
---

# PINIT_ONCE_FN callback function


## -description

An application-defined callback function. Specify a pointer to this function when calling the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-initonceexecuteonce">InitOnceExecuteOnce</a> function. The <b>PINIT_ONCE_FN</b> type defines a pointer to this callback function. 
<b>InitOnceCallback</b> is a placeholder for the application-defined function name.

## -parameters

### -param InitOnce [in, out]

A pointer to the one-time initialization structure.

### -param Parameter [in, out, optional]

An optional parameter that was passed to the callback function.

### -param Context [out, optional]

The data to be stored with the one-time initialization structure. If  <i>Context</i>  references a value, the low-order <b>INIT_ONCE_CTX_RESERVED_BITS</b> of the value must be zero. If  <i>Context</i>  points to a data structure, the data structure must be <b>DWORD</b>-aligned. <i>Context</i> must not be a code pointer on Arm32, because Arm32 code pointers always have the least significant bit set, see the <a href="/cpp/build/overview-of-arm-abi-conventions?view=msvc-170#instruction-set">Arm32 ABI</a> for details.

## -returns

If the function returns <b>TRUE</b>, the block is marked as initialized.

If the function returns <b>FALSE</b>, the block is not marked as initialized and the call to <a href="/windows/desktop/api/synchapi/nf-synchapi-initonceexecuteonce">InitOnceExecuteOnce</a> fails. To communicate additional error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> before returning <b>FALSE</b>.

## -remarks

This function can create a synchronization object and return it in the <i>lpContext</i> parameter.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.


#### Examples

For an example that uses 
this function, see 
<a href="/windows/desktop/Sync/using-one-time-initialization">Using One-Time Initialization</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/synchapi/nf-synchapi-initonceexecuteonce">InitOnceExecuteOnce</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-initonceinitialize">InitOnceInitialize</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
