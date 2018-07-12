---
UID: NF:winbase.DisableThreadProfiling
title: DisableThreadProfiling function
author: windows-sdk-content
description: Disables thread profiling.
old-location: hcp\disablethreadprofiling.htm
old-project: hcp
ms.assetid: 650631a6-fd90-46e1-8f2d-84aaaed05bac
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: DisableThreadProfiling, DisableThreadProfiling function [Hardware Counter Profiling], hcp.disablethreadprofiling, winbase/DisableThreadProfiling
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - DisableThreadProfiling
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# DisableThreadProfiling function


## -description


Disables thread profiling.


## -parameters




### -param PerformanceDataHandle [in]

The handle that the <a href="https://msdn.microsoft.com/dbbe5b01-cabf-42cb-9ed9-c2c143f9923b">EnableThreadProfiling</a> function returned.


## -returns



 Returns ERROR_SUCCESS if the call is successful; otherwise, a system error code (see Winerror.h).




## -remarks



You must call this function from the same thread that enabled profiling for the specified handle. You must call this function before exiting the thread; otherwise, you will leak resources (the resources are not reclaimed until the process exits).




## -see-also




<a href="https://msdn.microsoft.com/dbbe5b01-cabf-42cb-9ed9-c2c143f9923b">EnableThreadProfiling</a>



<a href="https://msdn.microsoft.com/cf746694-cc3a-4791-8877-fd879e968811">QueryThreadProfiling</a>
 

 

