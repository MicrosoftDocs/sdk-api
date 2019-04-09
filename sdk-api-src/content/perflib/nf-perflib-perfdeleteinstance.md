---
UID: NF:perflib.PerfDeleteInstance
title: PerfDeleteInstance function (perflib.h)
author: windows-sdk-content
description: Deletes an instance of the counter set created by the PerfCreateInstance function.
old-location: perf\perfdeleteinstance.htm
tech.root: perfctrs
ms.assetid: 8266e58c-c0a3-42dd-9f06-0d04dccfcf7c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PerfDeleteInstance, PerfDeleteInstance function [Perf], base.perfdeleteinstance, perf.perfdeleteinstance, perflib/PerfDeleteInstance
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
 - PerfDeleteInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PerfDeleteInstance function


## -description


Deletes an instance of the counter set  created by the <a href="https://msdn.microsoft.com/73be8588-2c87-4c27-933d-62b8605ed9a3">PerfCreateInstance</a> function.   Providers use this function.


## -parameters




### -param Provider [in]

The handle of the provider. Use the handle variable that the <a href="https://msdn.microsoft.com/3939f6a1-0a94-429d-a71e-b37f045fea13">CTRPP</a> tool generated for you. For the name of the variable, see the <b>symbol</b> attribute of the <a href="https://msdn.microsoft.com/10112f43-f483-4ecb-aa7d-60efaad149c6">provider</a> element.

<b>Windows Vista:  </b>The <a href="https://msdn.microsoft.com/b417b19b-adbc-40e3-aca1-c2cd94a79232">PerfStartProvider</a> function returns the handle.


### -param InstanceBlock [in]

A <a href="https://msdn.microsoft.com/709d5339-cedd-4b03-9d8e-c125eb3bcac0">PERF_COUNTERSET_INSTANCE</a> structure that contains the instance of the counter set to delete.


## -returns



If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. 




## -remarks



If the provider process terminates abnormally, all allocated instances will be released.

The provider determines when it deletes an instance. If the counter data is more static, the provider can delete an instance at cleanup time. For example, the number of processors on a computer would be considered static, so a provider that provides counter data for processors could delete an instance for each processor on the computer at cleanup time. For counters that are more dynamic, such as disk or process counters, the providers would delete the instances in response to a USB device being removed or a process being terminated.




## -see-also




<a href="https://msdn.microsoft.com/73be8588-2c87-4c27-933d-62b8605ed9a3">PerfCreateInstance</a>



<a href="https://msdn.microsoft.com/844f3f9e-8de2-4995-b13c-befe0da8a1ab">PerfQueryInstance</a>
 

 

