---
UID: NF:winnt._InlineInterlockedAdd64
title: _InlineInterlockedAdd64 function (winnt.h)
author: windows-sdk-content
description: Performs an atomic addition operation on the specified LONGLONG values.
old-location: base\interlockedadd64.htm
tech.root: Sync
ms.assetid: ab37292f-4291-4cca-826c-d6488e141db8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InterlockedAdd64, InterlockedAdd64 function, _InlineInterlockedAdd64, base.interlockedadd64, winnt/InterlockedAdd64
ms.topic: function
f1_keywords: ["winnt/InterlockedAdd64"]
req.header: winnt.h
req.include-header: Windows.h
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
 - InterlockedAdd64
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# _InlineInterlockedAdd64 function


## -description


Performs an atomic addition operation on the specified <b>LONGLONG</b> values.


## -parameters




### -param Addend [in, out]

A pointer to the first operand. This value will be replaced with the result of the operation.


### -param Value [in]

The second operand.


## -returns



The function returns the result of the operation.




## -remarks



The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="https://docs.microsoft.com/previous-versions//51s265a6(v=vs.85)">_InterlockedAdd64</a>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-interlockedadd">InterlockedAdd</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-_inlineinterlockedadd">InterlockedAddAcquire</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms683510(v=vs.85)">InterlockedAddAcquire64</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh972629(v=vs.85)">InterlockedAddNoFence</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh972630(v=vs.85)">InterlockedAddNoFence64</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms683513(v=vs.85)">InterlockedAddRelease</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms683514(v=vs.85)">InterlockedAddRelease64</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-interlockedexchangeadd">InterlockedExchangeAdd</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
 

 

