---
UID: NF:winbase.QueryThreadProfiling
title: QueryThreadProfiling function (winbase.h)
author: windows-sdk-content
description: Determines whether thread profiling is enabled for the specified thread.
old-location: hcp\querythreadprofiling.htm
tech.root: hcp
ms.assetid: cf746694-cc3a-4791-8877-fd879e968811
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: QueryThreadProfiling, QueryThreadProfiling function [Hardware Counter Profiling], hcp.querythreadprofiling, winbase/QueryThreadProfiling
ms.topic: function
f1_keywords: 
 - "winbase/QueryThreadProfiling"
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
 - QueryThreadProfiling
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# QueryThreadProfiling function


## -description


Determines whether thread profiling is enabled for the specified thread.


## -parameters




### -param ThreadHandle [in]

The handle to the thread of interest.


### -param Enabled [out]

Is <b>TRUE</b> if thread profiling is enabled for the specified thread; otherwise, <b>FALSE</b>.


## -returns



 Returns ERROR_SUCCESS if the call is successful; otherwise, a system error code (see Winerror.h).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-disablethreadprofiling">DisableThreadProfiling</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-enablethreadprofiling">EnableThreadProfiling</a>
 

 

