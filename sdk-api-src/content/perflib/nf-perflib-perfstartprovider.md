---
UID: NF:perflib.PerfStartProvider
title: PerfStartProvider function (perflib.h)
author: windows-sdk-content
description: Registers the provider.
old-location: perf\perfstartprovider.htm
tech.root: perfctrs
ms.assetid: b417b19b-adbc-40e3-aca1-c2cd94a79232
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PerfStartProvider, PerfStartProvider function [Perf], base.perfstartprovider, perf.perfstartprovider, perflib/PerfStartProvider
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
 - PerfStartProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PerfStartProvider function


## -description


Registers the provider.


## -parameters




### -param ProviderGuid [in]

GUID that uniquely identifies the provider. The <b>providerGuid</b> attribute of the <a href="https://msdn.microsoft.com/10112f43-f483-4ecb-aa7d-60efaad149c6">provider</a> element specifies the GUID.


### -param ControlCallback [in, optional]


<a href="https://msdn.microsoft.com/0f771ab7-af42-481b-b2da-20dcdf49b82b">ControlCallback</a> function that PERFLIB calls to notify you of consumer requests, such as a request to add or remove counters from the query. This parameter is set if the <b>callback</b> attribute of the <b>counters</b> element is "custom"; otherwise, <b>NULL</b>. 


### -param phProvider [out]

Handle to the provider. You must call <a href="https://msdn.microsoft.com/4b31f88b-cadc-4bee-bdea-9079cc14c140">PerfStopProvider</a> to release resources associated with the handle.


## -returns



If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. 




## -remarks



The <a href="https://msdn.microsoft.com/edcf8df3-0f6d-4849-b41d-270509499b8e">CounterInitialize</a> function calls this function; do not call this function directly.

<b>Windows Vista:  </b>The <b>PerfAutoInitialize</b> function calls this function.




## -see-also




<a href="https://msdn.microsoft.com/4b31f88b-cadc-4bee-bdea-9079cc14c140">PerfStopProvider</a>
 

 

