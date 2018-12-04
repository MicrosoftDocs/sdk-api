---
UID: NC:synchapi.PINIT_ONCE_FN
title: PINIT_ONCE_FN
author: windows-sdk-content
description: An application-defined callback function. Specify a pointer to this function when calling the InitOnceExecuteOnce function.
old-location: base\initoncecallback.htm
tech.root: sync
ms.assetid: e4a73572-e477-4518-87fe-b9b74234e8ec
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: PINIT_ONCE_FN, PINIT_ONCE_FN callback, PINIT_ONCE_FN callback function, base.initoncecallback, synchapi/PINIT_ONCE_FN
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - synchapi.h
api_name:
 - PINIT_ONCE_FN
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PINIT_ONCE_FN callback function


## -description


An application-defined callback function. Specify a pointer to this function when calling the 
<a href="https://msdn.microsoft.com/04c161ed-d1b0-4995-b246-cb64cb67ae47">InitOnceExecuteOnce</a> function. The <b>PINIT_ONCE_FN</b> type defines a pointer to this callback function. 
<b>InitOnceCallback</b> is a placeholder for the application-defined function name.


## -parameters




### -param InitOnce [in, out]

A pointer to the one-time initialization structure.


### -param Parameter [in, out, optional]

An optional parameter that was passed to the callback function.


### -param *Context [out, optional]

The data to be stored with the one-time initialization structure. If  <i>Context</i>  references a value, the low-order <b>INIT_ONCE_CTX_RESERVED_BITS</b> of the value must be zero. If  <i>Context</i>  points to a data structure, the data structure must be <b>DWORD</b>-aligned.


## -returns



If the function returns <b>TRUE</b>, the block is marked as initialized.

If the function returns <b>FALSE</b>, the block is not marked as initialized and the call to <a href="https://msdn.microsoft.com/04c161ed-d1b0-4995-b246-cb64cb67ae47">InitOnceExecuteOnce</a> fails. To communicate additional error information, call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> before returning <b>FALSE</b>.




## -remarks



This function can create a synchronization object and return it in the <i>lpContext</i> parameter.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.


#### Examples

For an example that uses 
this function, see 
<a href="https://msdn.microsoft.com/47e68fbb-29f8-4930-beba-01d44263eb1e">Using One-Time Initialization</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/04c161ed-d1b0-4995-b246-cb64cb67ae47">InitOnceExecuteOnce</a>



<a href="https://msdn.microsoft.com/f2943ac5-0e43-4f07-8941-952383e2fa08">InitOnceInitialize</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

