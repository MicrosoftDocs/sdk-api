---
UID: NF:winbase.DisableThreadProfiling
title: DisableThreadProfiling function (winbase.h)
description: Disables thread profiling.
old-location: hcp\disablethreadprofiling.htm
tech.root: hcp
ms.assetid: 650631a6-fd90-46e1-8f2d-84aaaed05bac
ms.date: 12/05/2018
ms.keywords: DisableThreadProfiling, DisableThreadProfiling function [Hardware Counter Profiling], hcp.disablethreadprofiling, winbase/DisableThreadProfiling
ms.topic: function
f1_keywords:
- winbase/DisableThreadProfiling
dev_langs:
- c++
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
api_name:
- DisableThreadProfiling
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DisableThreadProfiling function


## -description


Disables thread profiling.


## -parameters




### -param PerformanceDataHandle [in]

The handle that the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-enablethreadprofiling">EnableThreadProfiling</a> function returned.


## -returns



 Returns ERROR_SUCCESS if the call is successful; otherwise, a system error code (see Winerror.h).




## -remarks



You must call this function from the same thread that enabled profiling for the specified handle. You must call this function before exiting the thread; otherwise, you will leak resources (the resources are not reclaimed until the process exits).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-enablethreadprofiling">EnableThreadProfiling</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-querythreadprofiling">QueryThreadProfiling</a>
 

 

