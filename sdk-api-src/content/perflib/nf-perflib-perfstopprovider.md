---
UID: NF:perflib.PerfStopProvider
title: PerfStopProvider function
author: windows-sdk-content
description: Removes the provider's registration from the list of registered providers and frees all resources associated with the provider.
old-location: perf\perfstopprovider.htm
tech.root: perfctrs
ms.assetid: 4b31f88b-cadc-4bee-bdea-9079cc14c140
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: PerfStopProvider, PerfStopProvider function [Perf], base.perfstopprovider, perf.perfstopprovider, perflib/PerfStopProvider
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: perflib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Core-perfcounters-l1-1-0.dll
 - KernelBase.dll
api_name:
 - PerfStopProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PerfStopProvider function


## -description


Removes the provider's registration from the list of registered providers and frees all resources associated with the provider.


## -parameters




### -param ProviderHandle [in]

Handle to the provider. 


## -returns



If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. 




## -remarks



The <a href="https://msdn.microsoft.com/e52c1ee0-140a-4277-bddd-d93338a512bc">CounterCleanup</a> function calls this function; do not call this function directly.

<b>Windows Vista:  </b>The <b>PerfAutoCleanup</b> function calls this function.




## -see-also




<a href="https://msdn.microsoft.com/b417b19b-adbc-40e3-aca1-c2cd94a79232">PerfStartProvider</a>
 

 

