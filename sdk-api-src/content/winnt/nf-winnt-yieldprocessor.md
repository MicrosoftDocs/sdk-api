---
UID: NF:winnt.YieldProcessor
title: YieldProcessor function (winnt.h)
author: windows-sdk-content
description: Signals to the processor to give resources to threads that are waiting for them.
old-location: base\yieldprocessor.htm
tech.root: Sync
ms.assetid: 83a331c1-cfc6-427d-aa80-9583db02ee92
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: YieldProcessor, YieldProcessor function, base.yieldprocessor, winnt/YieldProcessor
ms.topic: function
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - YieldProcessor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# YieldProcessor function


## -description


Signals to the processor to give resources to threads that are waiting for them. This macro is only effective on processors that  support technology allowing multiple threads running on a single processor, such as Intel's Hyperthreading technology.


## -parameters






## -returns



This function does not return a value.




## -remarks



This macro can be called on all processor platforms where Windows is supported, but  it  has no effect on some platforms.  The definition varies from platform to platform. The following are some definitions of this macro in Winnt.h:

<pre class="syntax" xml:space="preserve"><code>#define YieldProcessor() __asm { rep nop }

#define YieldProcessor _mm_pause

#define YieldProcessor __yield
</code></pre>


