---
UID: NF:winnt.TpInitializeCallbackEnviron
title: TpInitializeCallbackEnviron function
author: windows-sdk-content
description: Initializes a callback environment for the thread pool.
old-location: base\tpinitializecallbackenviron.htm
old-project: procthread
ms.assetid: 4602CB19-D8C0-460E-A853-8DDECE643A76
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TpInitializeCallbackEnviron, TpInitializeCallbackEnviron function, base.tpinitializecallbackenviron, winnt/TpInitializeCallbackEnviron
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnt.h
req.include-header: 
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: TRANSACTION_OUTCOME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winnt.h
api_name:
 - TpInitializeCallbackEnviron
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# TpInitializeCallbackEnviron function


## -description


Initializes a callback environment for the thread pool.


## -parameters




### -param CallbackEnviron [out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. Allocate space for this structure and initialize it using this function.


## -returns



This function does not return a value.




## -remarks



The thread pool callback environment is subject to default behaviors that can be changed. For example, callbacks execute in the global pool by default, but a different thread pool can be specified using <a href="https://msdn.microsoft.com/A1BED20A-9DB5-4B5A-B1AD-60454176AB1D">TpSetCallbackThreadpool</a>. Thread pool callback environment behavior can be changed with the following functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/C4715789-0DF7-436B-881F-4360A7528246">TpSetCallbackActivationContext</a>
</li>
<li>
<a href="https://msdn.microsoft.com/B14084F5-2686-4522-8024-71A07541CFE2">TpSetCallbackCleanupGroup</a>
</li>
<li>
<a href="https://msdn.microsoft.com/425898A7-5E98-490A-912A-A409D1E2DFDE">TpSetCallbackFinalizationCallback</a>
</li>
<li>
<a href="https://msdn.microsoft.com/27E7F647-1005-4499-9787-F2CE6E8B6AFF">TpSetCallbackLongFunction</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8415197A-C785-492E-9C74-2055FADDF0CD">TpSetCallbackNoActivationContext</a>
</li>
<li>
<a href="https://msdn.microsoft.com/FE2CB959-25BC-4420-A921-2A65016B25CF">TpSetCallbackPersistent</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3A2DA8CA-D5F2-442A-B152-11AB28681B5B">TpSetCallbackPriority</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14519064-450C-409E-AA2D-B4EF4D43C180">TpSetCallbackRaceWithDll</a>
</li>
<li>
<a href="https://msdn.microsoft.com/A1BED20A-9DB5-4B5A-B1AD-60454176AB1D">TpSetCallbackThreadpool</a>
</li>
</ul>
Call
<b>TpInitializeCallbackEnviron</b>to create a callback environment that can be modified. Call <a href="https://msdn.microsoft.com/B0925491-73FE-4342-9E66-E5F6344353FB">TpDestroyCallbackEnviron</a> to destroy the callback environment.

This function is implemented as an inline function.



